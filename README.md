
# Cartoon Character Recognition

A brief description of what this project does and who it's for

Project Usage Guide
Running the Script
Some issues were encountered when requesting image input interactively. Therefore, the recommended way to run the script is:

Place the image(s) inside the ./test/ folder in .jpg format.
(Optional) You can also test directly from the TRAIN dataset using:

matlab   imageFolder = fullfile('TRAIN', 'Bob esponja');
3. Execute only **Parts 0, 1, and 3** of the script.
4. Press any key to move to the next image.

---

## Notes

- The descriptors used in the report are slightly different from the current ones, although the differences are minimal.
- When generating new descriptors for testing, consider saving them under a **different name** to avoid overwriting existing files.

---

## Script Structure

To run a full experiment or test the code, only **Part 2** needs to be modified. The script is organized as follows:

| Part | Name | Description |
|------|------|-------------|
| **Part 0** | Input Table | Contains the base TRAIN dataset. |
| **Part 1** | Model Training | The model function has been externalized so it can be computed in situ, allowing verification of parameters and ensuring model validity. |
| **Part 2** | Point Selection | Two precomputed descriptors are included in the `.zip`, so this section can be skipped if desired. However, the code is designed to work in any environment and demonstrate that descriptors are not preloaded unfairly. |
| **Part 3** | Output | Handles the Series Image + Characters output. Should work correctly as long as the required files are present. |

### Expected Folder Structure (Part 2)
```
./personatgeEntrenament/personatge<i>/imatge<j>.jpg
```

> Where `personatge<i>` is the character name **without spaces**.

---

### Required Files for Part 3

The following files must be present in the directory:
```
descriptors_personatge<i>.mat

These files are generated in Part 2 and are already included in the .zip.