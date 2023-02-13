### Hi there 👋


- 🔭 I’m currently working on DeepLearning.
- 🌱 I’m currently learning Open CV and Recommender Systems.
- 👯 I’m looking to collaborate on Deep Learning.
- 🤔 I’m looking for help with Advanced Machine Learning.
- 💬 Ask me about Astronomy and History
- 📫 How to reach me: vishnu.v5next@gmail.com
- 😄 Pronouns: V--ish--nnu.
- ⚡ Fun fact: At the end of every black hole is a white hole, creating a new universe in the rift of space. In One I am the BATMAN




import React, { useState } from 'react';

type MultiLevelDropdownItem = string | { [key: string]: MultiLevelDropdownItem[] };

interface Props {
  items: MultiLevelDropdownItem[];
  onChange?: (value: string) => void;
}

const MultiLevelDropdown: React.FC<Props> = ({ items, onChange }) => {
  const [isOpen, setIsOpen] = useState(false);
  const [selectedValue, setSelectedValue] = useState('');

  const handleSelect = (value: string) => {
    setSelectedValue(value);
    setIsOpen(false);
    onChange && onChange(value);
  };

  const renderDropdown = (data: MultiLevelDropdownItem[], level = 0) => {
    return data.map((item, index) => {
      if (typeof item === 'string') {
        return (
          <li key={index}>
            <button
              onClick={() => handleSelect(item)}
              style={{ paddingLeft: level * 10 }}
            >
              {item}
            </button>
          </li>
        );
      } else {
        const [key, value] = Object.entries(item)[0];
        return (
          <li key={index}>
            {key}
            <ul>
              {renderDropdown(value, level + 1)}
            </ul>
          </li>
        );
      }
    });
  };

  return (
    <div>
      <button onClick={() => setIsOpen(!isOpen)}>
        Dropdown ({selectedValue || 'Select a value'})
      </button>
      {isOpen && (
        <ul>
          {renderDropdown(items)}
        </ul>
      )}
    </div>
  );
};

export default MultiLevelDropdown;
