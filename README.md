# taha-demo
<h>If you are not interested in it then you allowed to go</h>
<body>
   <h1>Recommended Books</h1>
   <?php 
   $books = [
       [
           'name' => 'Do Androids Dream of Electric Sheep',
           'author' => 'Philip K. Dick',
           'releaseYear' => 2021,
           'purchaseUrl' => 'http://example.com'
       ],
       [
           'name' => 'Project Hail Mary',
           'author' => 'Andy Weir',
           'releaseYear' => 1999,
           'purchaseUrl' => 'http://example.com'
       ],
       [
           'name' => 'The Martian',
           'author' => 'Andy Weir',
           'releaseYear' => 2011,
           'purchaseUrl' => 'http://example.com'
       ]
   ];

   // Function to check if a book is written by a specific author
   function isWrittenBy($book, $authorName) {
       return $book['author'] === $authorName;
   }

   $specificAuthor = 'Andy Weir'; // Change this to the author's name you want to check
   ?>
   <ul>
       <?php foreach ($books as $book): ?>
           <li>
               <a href="<?= $book['purchaseUrl'] ?>">
                   <?= $book['name']; ?> (<?= $book['releaseYear']; ?>)
               </a>
               <?php if (isWrittenBy($book, $specificAuthor)): ?>
                   <strong>- Written by <?= $specificAuthor; ?></strong>
               <?php endif; ?>
           </li>
       <?php endforeach; ?>
   </ul>
</body>
