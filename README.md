# Belajar Ansible

### Aplikasi yang harus diinstall
- vagrant/vps (untuk lab sendiri)
- virtualbox (untuk menjalankan vagrant)
- ansible

## Cara Menggunakan
- Jalankan vagrant
  - ``` vagrant up ```
- Buat file ssh key
  - ``` ssh-keygen ```
- Copy file ``` ~/.ssh/id_rsa.pub``` kedalam vagrant di file ``` ~/.ssh/authorized_keys ```
- Test Ansible terlebih dahulu
  - ``` ansible root -m ping ```
  - Jika berhasil akan tampil seperti berikut
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_01.png)
- Menjalankan ansible
  - ``` ansible-playbook -s master.yml ```
