Pagination Helper

    class PaginationHelper {
      constructor(collection, itemsPerPage) {
        this.collection = collection;
        this.itemsPerPage = itemsPerPage;
      }
    
      itemCount() {
        return this.collection.length;
      }
    
      pageCount() {
        return Math.ceil(this.itemCount() / this.itemsPerPage);
      }
    
      pageItemCount(pageIndex) {
        if (pageIndex < 0 || pageIndex >= this.pageCount()) {
          return -1;
        }
        if (pageIndex === this.pageCount() - 1) {
          return this.itemCount() % this.itemsPerPage || this.itemsPerPage;
        }
        return this.itemsPerPage;
      }
    
      pageIndex(itemIndex) {
        if (itemIndex < 0 || itemIndex >= this.itemCount()) {
          return -1;
        }
        return Math.floor(itemIndex / this.itemsPerPage);
      }
    }
    
    // Example usage
    var helper = new PaginationHelper(['a', 'b', 'c', 'd', 'e', 'f'], 4);
    console.log(helper.pageCount());        // Output: 2
    console.log(helper.itemCount());        // Output: 6
    console.log(helper.pageItemCount(0));   // Output: 4
    console.log(helper.pageItemCount(1));   // Output: 2
    console.log(helper.pageItemCount(2));   // Output: -1
    console.log(helper.pageIndex(5));       // Output: 1
    console.log(helper.pageIndex(2));       // Output: 0
    console.log(helper.pageIndex(20));      // Output: -1
    console.log(helper.pageIndex(-10));     // Output: -1
