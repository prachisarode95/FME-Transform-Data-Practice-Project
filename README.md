# 🌍 FME Project: Transforming Web Data with Attribute Filtering

## 📘 About the Project

This project is a hands-on exercise from the **FME Form Basic course** by Safe Software, under the "Transform Data" path. It demonstrates how to read JSON data from an API, extract and transform spatial and non-spatial data, join it with local datasets, and output a cleaned and sorted result. The entire workflow was built and executed using **FME Workbench 2024.2**, showcasing real-world data integration and transformation techniques.

---

## 🛠️ Tools Used

- **FME Workbench**  
  For designing, building, and executing the data transformation workflow.

- **FME Data Inspector**  
  To inspect the final output of the project after running the workspace successfully.

---

## 🔄 Workflow Overview

![Image](https://github.com/user-attachments/assets/8ac4e0f0-aa73-45ec-8521-36ab971d9bbc)

The data transformation process followed these steps:

1. **Fetch JSON Data** using `HTTPCaller` from a web URL.
2. **Parse JSON** with `JSONFragmenter` to extract individual records.
3. **Create Geometries** using coordinates with `VertexCreator`.
4. **Set Coordinate System** to ensure proper spatial referencing.
5. **Manage Attributes** to clean and prepare data for joining.
6. **Join Web Data with Local Data** using `DatabaseJoiner`.
7. **Remove Unwanted Attributes** using `AttributeRemover`.
8. **Sort Features Alphabetically** by `last_name` using `Sorter`.
9. **Filter Final Output** using `Tester` before writing the final data to output.

---

## 🧰 Transformers Applied

| Transformer            | Purpose                                                                 |
|------------------------|-------------------------------------------------------------------------|
| `Creator`              | Starts the workflow                                                     |
| `HTTPCaller`           | Fetches live data from a web API                                        |
| `JSONFragmenter`       | Parses JSON and extracts data records                                   |
| `VertexCreator`        | Converts coordinate values into spatial geometries                      |
| `CoordinateSystemSetter` | Assigns a spatial reference system                                     |
| `AttributeManager`     | Renames, reorders, or removes unnecessary attributes                     |
| `DatabaseJoiner`       | Joins web data with an external dataset                                 |
| `AttributeRemover`     | Removes attributes like `_matched_records` before output                |
| `Sorter`               | Sorts data alphabetically based on the `last_name` attribute            |
| `Tester`               | Filters valid records before writing to output                          |

---

## 🧾 Key Output

- A cleaned, filtered, and alphabetically sorted dataset of business owners.
- Only selected attributes (`first_name`, `last_name`, `company`, `license_number`) are included.
- Unnecessary technical fields (e.g., `_matched_records`) are removed from the output.

---

## 💡 Learnings & Reflection

✔️ Gained experience working with web APIs inside FME  
✔️ Learned how to join external and internal datasets using key fields  
✔️ Understood the importance of attribute management in clean data delivery  
✔️ Practiced layout organization, annotation, and efficient workspace execution  
✔️ Completed the project with real-time execution captured on video, validating my practical FME skills

---

## 🔗 LinkedIn / Demo

- 🎥 [Watch Workspace Running in FME Workbench](https://github.com/user-attachments/assets/b592e7fd-39fc-4f47-8ee1-c8b9ca6b057d)  
- 🎥 [Watch Final Output with Sorted Data in FME Data Inspector](https://github.com/user-attachments/assets/19ac9722-8a62-4abd-b245-282a6cb6369b)

---



