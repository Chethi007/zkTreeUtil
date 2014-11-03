==========================================
zkTreeUtil - ZooKeeper Tree Utility
Author: Dobrunov Aleksey (ctapmex)
==========================================

zkTreeUtil ��� ���������� ��� ������ � �������/�������, ��������� � ZooKeeper.
������� �������� ������ - ������� ����������� ZooKeeper.

usage: zkTreeUtil
 -e,--export                       exports the zookeeper tree
 -od,--output-dir <dir>            output directory to which znode
                                   information should be written (must be
                                   a normal, empty directory)
 -of,--output-file <filename>      output file to which znode information
                                   should be written
 -p,--path <znodepath>             path to the zookeeper subtree rootnode.
 -xf,--output-xmlfile <filename>   output xml-file to which znode
                                   information should be written
 -z,--zookeeper <zkhosts>          zookeeper remote servers (ie
                                   "localhost:2181")

������� ������������ � ���� ��������:
 - �������� ��������� (output-dir) 
    � �������� ��� ������ ����������, ��� ������� ���� ��������� ���� �����, 
    ���� ����. �������� ����������� ���������. ���� ��� ���� ������ ��������
    (value), �� ��� ����������� � ����. ��� �����-����� �������� ����������� �
    ���� '_znode'.
    ������� ����������� ������� ������� - �������� ������ ������������ �� ��� 
    ������� � �����. �������� ':'.
 - ������� ���� (output-file)
    � �������� ��� ������ �����, ��������� ������ ����
    path=/ss	val=dd	type='ephemeral'
    path - ���� ����.
    val - ��������, ���� ������
    type - ��� ����. ephemeral - ���������/��������� ����.
 - xml ����  
    � �������� ��� ������ �����, ��������� ���� (znode), �������� ���
    ���������� � ���������

��� ����������� �������� ������������� ��������� ZooKeeper, ������������ ���� 'p'.
�������� 'z', ����� �������, ������������ �������� ���������� ��������
�������� ZooKeeper ����� �������. ��������, 127.0.0.1:3000,127.0.0.1:3001

������� �������������:
zktreeutil -z 127.0.0.1:2181 --export -xf d:\test.xml -p /ss
zktreeutil -z 127.0.0.1:2181 --export -od d:\test

���������� �� ������
------------------
1. ����� � ���������� � �����������
2. mvn clean package
3. ����������� 'zkTreeUtil' ����� ������ � ���������� target\distrib

