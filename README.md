# ssh-keygen
# ПЕРВОЕ
ssh-keygen -t rsa -b 4096 -C "ПОЧТА ПРИВЯЗАННАЯ К ГИТХАБУ ИДИОТ"
# Второе
eval $(ssh-agent -s)
# ТРЕТЬЕ
ssh-add ~/.ssh.id_rsa
# Четвёртое
Копируем публичный ключ командой cat ~/.ssh/id_rsa.pub
Идём в гитхаб и вставляем в new ssh 
