#DB STRUCURE


##mapod4d models
Madopd4d core and relative versions rappresentation

##Table: Mapod4d
####Field: name CharField(max_length=21, null=False, unique=True, validators=[alphanumeric])
Name of mapod4d core
####Field: description TextField(max_length=200, default='')
Description

##Table: Mapod4dVersion
####Field: link URLField(default='')
Link to download the MAPOD4D application
####Field: v1 PositiveIntegerField(default=0, null=False)
Version component v1.v2.v3.v4p
####Field: v2 PositiveIntegerField(default=0, null=False)
Version component v1.v2.v3.v4p
####Field: v3 PositiveIntegerField(default=0, null=False)
Version component v1.v2.v3.v4p
####Field: v4 PositiveIntegerField(default=0, null=False)
Version component v1.v2.v3.v4p
####Field: p CharField(max_length=2, default="s", null=False)
Version component v1.v2.v3.v4p
####Field: bricks PositiveIntegerField(default=1, null=False)
Number of files in which the download file is splitted
####Field: compress BooleanField(default=False, null=False)
true if the file is compressed
####Field: value PositiveIntegerField(null=False)
Draft
####Field: mapod4d ForeignKey('Mapod4d', on_delete=models.CASCADE)
Relation 1:N with Table Mapod4d field id

###Constraints
UniqueConstraint('v1', 'v2', 'v3', 'v4',  name='mapod4d_version')

---
