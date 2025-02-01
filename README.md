Alumna: Betlem Ferrer

¿Qué comando utilizaste en el **paso 11**? ¿Por qué? 
git reset –-hard HEAD 1 Deshace el último commit y lo que había en la working copy de manera que todo 
quede como estaba antes. Nuestro staging área queda vacío. Se modifica el working copy. 
Se usa para modificaciones experimentales y al final queremos dejarlo tal y como está.

¿Qué comando o comandos utilizaste en el **paso 12**? ¿Por qué?
git reflog
git reset --hard 383144c
Primero ver el reflog y localizar el commit que teníamos antes. Después, con el git reset --hard, localizarlo.

El merge del **paso 13**, ¿Causó algún conflicto? ¿Por qué? 
git merge master
Already up to date.
El merge ha causado un error que me dice que la rama actual ya tiene todos los commits que están en la rama master.
El merge no aportará nada nuevo.



El merge del **paso 19**, ¿Causó algún conflicto? ¿Por qué?
$ git merge htmlify
Auto-merging git-nuestro.md
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.
Se crea un conflicto porque en dos commits hay líneas diferentes y git no sabe cuáles son las buenas.
Resuelvo el conflicto quedándome con la versión de "styled".


El merge del **paso 21**, ¿Causó algún conflicto? ¿Por qué? 
No, no causó conflictos. 
He utilizado: git merge styled desde la rama master
git merge styled
Updating 60b5b05..75ad164
Fast-forward
 git-nuestro.md | 19 ++++++++++---------
 1 file changed, 10 insertions(+), 9 deletions(-)




¿Qué comando o comandos utilizaste en el **paso 25**?

git log --graph --decorate --pretty=oneline

*   75ad16411ffcd6eac3411e797a19c25245830be0 (HEAD -> master, styled) Merge branch 'htmlify' into styled
|\
| * 4d7136dbc1058b1cf914481b9045a4c3525f1ebe (htmlify) Añado  la tercera versión de git-nuestro, con html
* | 383144cad1fbd17891f406753b07fcbd4f94bec1 Añado segunda versión de git-nuestro
|/
* 60b5b05d44823d5478707f7eea11ec23ae136d6c Añado primera versión de git-nuestro


El merge del **paso 26**, ¿Podría ser fast forward? ¿Por qué?
Sí que podría ser Fast Forward, también. Porque sería sólo un cambio de puntero Master y HEAD al commit D (el de Title).


¿Qué comando o comandos utilizaste en el **paso 27**? 
git reset --merge HEAD
Para deshacer el merge.


¿Qué comando o comandos utilizaste en el **paso 28**? 
git restore git-nuestro-freak.md
Aunque no estoy muy segura de si es correcto o no.


¿Qué comando o comandos utilizaste en el **paso 30**?
git reflog
git checkout a0f478f
He buscado con el reflog cuál es el Hash del merge anterior (el de Title) y he ido allí con el checkout.


¿Qué comando o comandos usaste en el **paso 32**?
git reflog
git checkout 60b5b05


¿Qué comando o comandos usaste en el **punto 33**?
git reflog
git checkout f839b82
Previous HEAD position was 60b5b05 Añado primera versión de git-nuestro
HEAD is now at f839b82 Añado el título solicitado al fichero



