# Belajar Ansible

### Aplikasi yang harus diinstall
- vagrant 2.0.2 (untuk lab sendiri)
- virtualbox 5.2.8 (untuk menjalankan vagrant)
- ansible 2.4.3.0

## Cara Menggunakan
- Jalankan vagrant
  - ``` vagrant up ```
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_02.png)
- Masuk ke mesin virtual yang kita bikin tadi dengan perintah
  - ``` vagrant ssh ```
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_03.png)
  - keluar dari mesin virtual tadi
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_04.png)

- Buat ssh key untuk login ssh ke mesin virtual, disini saya tidak pada posisi root tetapi pada posisi user biasa
  - ``` ssh-keygen ```
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_05.png)
    - Enter file in which to save the key (/home/angel/.ssh/id_rsa): (Enter)
    - pada Overwrite (y/n)? (Klik Y)
    - Enter passphrase (empty for no passphrase): (masukkan password bebas)
    - Enter same passphrase again: (Samakan password yang diatas)

- Copy file ``` ~/.ssh/id_rsa.pub``` kedalam vagrant di file ``` ~/.ssh/authorized_keys ```
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_06.png)
  - Paste ke mesin virtual sampe tampil seperti tampilan berikut
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_07.png)
- Test Ansible terlebih dahulu
  - ``` ansible root -m ping ```
  - Jika berhasil akan tampil seperti berikut
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_08.png)
- Menjalankan ansible
  - ``` ansible-playbook -s master.yml ```
  - ![alt tag](https://raw.githubusercontent.com/amanualt/learn-ansibleLEMP/master/screen/Selection_09.png)
