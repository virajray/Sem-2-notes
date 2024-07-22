Database එකේ data store වෙන්නෙ table වල නම් ඒක relational database එකක්

1. **<span style="background:#fdbfff">Attribute</span>:** Attributes are the properties that define or describe a relation. e.g.; ROLL_NO, NAME, ADDRESS, PHONE, AGE.
    
2. **<span style="background:#fdbfff">Relation Schema:</span>** A relation schema represents name of the relation with its attributes. e.g.; STUDENT (ROLL_NO, NAME, ADDRESS, PHONE and AGE) is relation schema for STUDENT. If a schema has more than 1 relation, it is called Relational Schema.
    
3. **<span style="background:#fdbfff">Tuple</span>:** Each row in the relation is known as tuple. The above relation contains 4 tuples, one of which is shown as:
    
 ex:
	| 0003 | Piyumi | Kandy | 0775015123 | 25 |

4. **<span style="background:#fdbfff">Relation Instance</span>:** The set of tuples of a relation at a particular instance of time is called as relation instance. Table 1 shows the relation instance of STUDENT at a particular time. It can change whenever there is insertion, deletion, or updation in the database.
    
5. **<span style="background:#fdbfff">Domain</span>:** Set of data values that could be inserted in to a field/column.<font color="#ffff00">(field/column  එකක store කලහැකි Data type එක/ data size එක)</font>
    
6. **<span style="background:#fdbfff">Degree</span>:** The number of attributes in the relation is known as degree of the relation. The STUDENT relation defined above has degree 5<font color="#ffff00">. ( relation එකකට සම්භන්දවෙලා තියන එක එක entity සංක්‍යාව.<br><br>
   ex: මේකෙනම් දෙකයි එතකොට )</font> 
![[Pasted image 20240721192241.png]]
- <span style="background:#fff88f">Binary</span>-relationship with two participants 
- <span style="background:#fff88f">Ternary</span>-relationship with three participants 
- <span style="background:#fff88f">Quaternary</span>-relationship with four participants

 ඊට අමතරව relationship එකක් එකම entity එකට reflect වෙනවනම් ඒක <span style="background:#fff88f">unary/recursive</span> 
![[Pasted image 20240721193113.png]]
 
1. **<span style="background:#fdbfff">Cardinality</span>:** The number of tuples or rows in a relation is known as cardinality. The STUDENT relation defined above has cardinality 4.

### on delete / on update

<font color="#fac08f">Foreign  keys එක්ක වැඩ කරද්දි,</font>

<span style="background:#ff4d4f">no action / restrict</span>   When a parent record is updated or deleted, NO ACTION means the database will not automatically do anything to the related child records.<font color="#ffff00">(මොකක් හරි ඩේට එකක් හරි ෆීල්ඩ් එකක් හරි අප්ට්ඩේට් හරි ඩිලීට් හරි කරාම ඒ ඩේට එක කනෙක්ට් වෙලා තියන අනිත් තැන්වල කිසි වෙනසක් වෙන්නෑ)</font>

<span style="background:#00ffab">cascade</span>  <font color="#ffff00">මොකක් හරි ඩේට එකක් හරි ෆීල්ඩ් එකක් හරි අප්ට්ඩේට් හරි ඩිලීට් හරි කරාම ඒ ඩේට එක කනෙක්ට් වෙලා තියන හැම තැනක්ම අප්ඩේට් ඩිලීට් වෙනවා</font>

<span style="background:#affad1">set default</span> <font color="#ffff00">මොකක් හරි ඩේට එකක් හරි ෆීල්ඩ් එකක් හරි අප්ට්ඩේට් හරි ඩිලීට් හරි කරාම ඒ ඩේට එක කනෙක්ට් වෙලා තියන තැන්වල, ඒ ඒ තැන්වල දාල තිබ්බ default value වලට revert වෙනවා</font>

<span style="background:#fdbfff">set null</span>  <font color="#ffff00">මොකක් හරි ඩේට එකක් හරි ෆීල්ඩ් එකක් හරි අප්ට්ඩේට් හරි ඩිලීට් හරි කරාම ඒ ඩේට එක කනෙක්ට් වෙලා තියන හැම තැනක්ම NULL වෙනවා</font>


##### Database (Implementation) Models 

• Hierarchical 
• Network 
• Relational 
• Object-oriented


