README

Project by: Devon Rousavy
V#: V00875549
class: ECE519C


Below is the details required to run the file which is a python notebook file and can be run from Jupyter notebook or google colab

The description of what each section of code does is briefly explained below.

Section 1: A single round of the SPN cipher is defined here i.e. XORs a key, inputs into the s-box and then permutes the output.

Section 2: Defines the full encryption function which uses the cipher_round function described above. This is where you can alter the 
keys for each round of the SPN.

Section 3: Not essential. Looks to verify that we do indeed get the same differential characterstics as those defined in the paper.

Section 4: Not essential. Displays the input difference between plaintexts and the 16 output differences. We can see that not all output differences
are equiprobable.

Section 5: The first part of the key retrieval. Uses input difference 0000 1011 0000 0000 to retrieve subkey block 2 and 4

Section 6: Not essential. Shows which subkey value (0-255) resulted in the most right-pairs i.e. the list with the most ones.

Section 7: Counts up the number of ones that each subkey value produces.

Section 7: Takes the subkey with the longest count and the subkey with the second longest count. In the event of a tie all pairs with
longest and second longest count lists are taken. These are the candidates for the subkey.

Section 8: The second part of the key retrieval. Uses input difference 0000 0000 0000 0010 to retrieve subkey blocks 1 and 3.

Section 9: Equivalent to section 6 but for the other subkey.

Section 10: Equivalent to section 7 but for the other subkey

Section 11: Produces the most probable values for the whole key. The most probable are labelled with the string possible keys. The 
secondary options (lower probability) are labelled less probable keys. In the event of ties there can be more than one key for each of
these possible key and less probably key outputs. Note some keys will stump the algorithm and not be retrieved but usually the key to
the final round will be output under the possible key section.

How to run: Simply put your key in as a string where it says k5 in section 2. You may also want to change the other round keys which is
again done by simply altering the string to the desired value. Do not enter values shorter or longer than 16 (binary) digits as the
program is not robust and will not run.

Once you have selected the desired keys for use in encryption simply run all cells sequentially (Run all) in your notebook program.

If there are any troubles running the program contact me through coursespaces and I will respond as soon as possible. 