### Hi there 👋


- 🔭 I’m currently working on DeepLearning.
- 🌱 I’m currently learning Open CV and Recommender Systems.
- 👯 I’m looking to collaborate on Deep Learning.
- 🤔 I’m looking for help with Advanced Machine Learning.
- 💬 Ask me about Astronomy and History
- 📫 How to reach me: vishnu.v5next@gmail.com
- 😄 Pronouns: V--ish--nnu.
- ⚡ Fun fact: At the end of every black hole is a white hole, creating a new universe in the rift of space. In One I am the BATMAN



ERROR in src/components/common/MultiDropDown.tsx:54:27
TS2345: Argument of type '(string | { [key: string]: (string | { [key: string]: (string | { [key: string]: string[]; })[]; })[]; })[]' is not assignable to 
parameter of type '(string | { [key: string]: string[]; })[]'.
  Type 'string | { [key: string]: (string | { [key: string]: (string | { [key: string]: string[]; })[]; })[]; }' is not assignable to type 'string | { [key: string]: string[]; }'.
    Type '{ [key: string]: (string | { [key: string]: (string | { [key: string]: string[]; })[]; })[]; }' is not assignable to type 'string | { [key: string]: string[]; }'.
      Type '{ [key: string]: (string | { [key: string]: (string | { [key: string]: string[]; })[]; })[]; }' is not assignable to type '{ [key: string]: string[]; }'.
        'string' index signatures are incompatible.
          Type '(string | { [key: string]: (string | { [key: string]: string[]; })[]; })[]' is not assignable to type 'string[]'.
            Type 'string | { [key: string]: (string | { [key: string]: string[]; })[]; }' is not assignable to type 'string'.
              Type '{ [key: string]: (string | { [key: string]: string[]; })[]; }' is not assignable to type 'string'.
    52 |       {isOpen && (
    53 |         <ul>
  > 54 |           {renderDropdown(items)}
       |                           ^^^^^
    55 |         </ul>
    56 |       )}
    57 |     </div>
