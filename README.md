# Enhancement Two: Algorithms and Data Structure

## **Introduction:**

The artifact selected for Enhancement One is `ItemAdapter.java` from my Inventory Application developed in CS 360: Mobile Architecture and Programming. The app as a whole acts as an inventory management solution that allows users to create, update, and track item quantities, and optionally receive SMS alerts for when items are out-of-stock. This adapter is responsible for displaying inventory items in a `ListView`, managing item deletion, and providing sorting and filtering functionality. The original implementation stored items in a `String[][]` array and reloaded the entire dashboard on deletion, which was functional but not scalable nor efficient. A new menu resource file (`sort_filter_menu.xml`) was also created to provide user-accessible sorting and filtering options via a `PopupMenu`. 

This artifact was selected for this enhancement because it aptly conveys my ability to apply algorithmic principles and implement efficient data structures in a practical application. 

## **Original Artifact:**

[Visit the Original Artifact (two files)](https://github.com/aricmoore/Enhancement-Two-Design/tree/main/Original)

<details>
  <summary><strong>Enhancement Goal</strong></summary>

This enhancement aimed to optimize `ItemAdapter.java` by implementing efficient data structures and algorithms for sorting, filtering, and deletion to improve both performance and scalability of the inventory dashboard.

</details>

## **Enhanced Artifact:**

[Visit the Enhanced Artifact (three files)](https://github.com/aricmoore/Enhancement-Two-Design/tree/main/Enhanced)

<details>
  <summary><strong>Design and Implementation</strong></summary>

The enhancement first replaced the `String[][]` array with a `List<InventoryItem>` to enable type safety, flexibility, and easier manipulation of data. New sorting methods (`sortByName`, `sortByQuantity`) utilize comparison-based algorithms with **O(n log n)** complexity, while filtering (`filterLowStock`) and deletion operations are **O(n)**. These improvements illustrate thoughtful consideration of algorithmic efficiency and scalability. 

The new XML menu (`sort_filter_menu.xml`) allows users to trigger these algorithms directly from the interface, which demonstrates linking data structure operations to UI interactions. Additionally, the deletion process was optimized to remove items from the list and notify the adapter, rather than reloading the entire dashboard; this showcases an understanding of performance and scalability considerations. 

With these changes, the artifact now reflects a better grasp of sound software engineering practices and separates the UI logic from data representation.

</details>

<details>
  <summary><strong>Reflections / Lessons Learned</strong></summary>

The process of enhancing this second artifact has taught me several key lessons. First, opting for a well-structured object-oriented data collection over a raw array helped clarify the practical advantages of type safety, readability, and maintainability. By implementing sorting and filtering, I was forced to consider algorithmic efficiency and user experience simultaneously. 

A challenge I faced was reconciling the new `List<InventoryItem>` approach with the existing dashboard code, particularly ensuring that UI updates reflected changes in the underlying data without any unnecessary reloads. Distinguishing data operations from UI updates helped me understand that a careful separation of concerns is absolutely critical when building scalable applications. 

While this process reinforced my understanding of both data structures and practical algorithm application, it also had the added benefit of highlighting the importance of incremental testing and verifying each change in the context of a larger system.

</details>

<details>
  <summary><strong>Course Outcomes</strong></summary>

This enhancement aligns with several course outcomes:
- **Outcome 1**: The process required coordinating the adapter, UI, and database logic, reflecting collaboration across different application layers.
- **Outcome 2**: Clear inline documentation, code comments, and narrative explanation demonstrate professional-quality communication suitable for a technical audience.
- **Outcome 3**: The use of structured objects and efficient sorting and filtering shows application of algorithmic principles, with explicit attention to trade-offs between simplicity, readability, and performance.
- **Outcome 4**: Adoption of modular design, `List` collections, and separation of UI from data demonstrates well-founded and maintainable techniques that deliver practical value.
- **Outcome 5**: Safe deletion operations, transactional database calls, and consistent state management reflect a security-conscious approach to software design.

</details>

- ---

<i>Thanks for stopping by! Check out my two other enhancements below:</i>
- [Enhancement One](https://github.com/aricmoore/Enhancement-One-Design)
- [Enhancement Three](https://github.com/aricmoore/Enhancement-Three-Design)

<sub>© 2026 Arielle Moore. All rights reserved. | CS 360: Mobile Architecture and Programming – Inventory Application | View my [portfolio](https://aricmoore.github.io/) for more projects.</sub>
