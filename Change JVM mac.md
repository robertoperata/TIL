### Change JVM
list JVM:
`/usr/libexec/java_home -V`

change JVM:
`export JAVA_HOME=$(/usr/libexec/java_home -v 17)`

configure persistently
```
nano ~/.zshrc
export JAVA_HOME=$(/usr/libexec/java_home -v 17)
export PATH=$JAVA_HOME/bin:$PATH
source ~/.zshrc

```
