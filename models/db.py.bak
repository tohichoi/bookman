db=DAL("sqlite://storage.sqlite")

db.define_table('books',
                Field('code'),
                Field('title'),
                Field('author'),
                Field('year'),
                Field('created_on', 'datetime', default=request.now),
                format='%(code) %(title)s')

db.books.code.requires=IS_NOT_IN_DB(db, db.books.code)
db.books.title.requires=IS_NOT_EMPTY()
db.books.author.requires=IS_NOT_EMPTY()
db.books.year.requires=IS_NOT_EMPTY()
