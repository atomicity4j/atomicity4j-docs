# Go history

- https://www.zhubert.com/blog/2014/01/12/introduction-to-go-golang-part-1/

# Why Go

- ������ ���������� ������
- Go ����� � �����


https://habrahabr.ru/post/261339/

- ������� ���� ��� ������ ������������ ������������ ���� ������� Go � �����, �������� � �������� � �����, �������� � ������� Unix, ����� C � UTF-8, � ������ ���������� ��� ��������� ���������� Google. ��� ��� �����, �� Go ������ � ��������� ������� ����������� ������, ������� ������ ������� ��������� � ������ �������, ������� ��������� ������������ �������� ���� ���������� ��.
- � ��� ������ ��, ��� ��������������� ��� �������� ���������� � ��������� Go. ���������� ���������. ���������� ������� ����������� ������������������ ������������ ��� ��������� ������������������ �������, ����������� ������� ������. ���������� ������ ������. ���������� ������� � ������ �� �������� ��������. ���������� ������ ������ ��� ����� � ���������. ���������� ������� �� �������� �����. � ��� �����, � ���� ��������.
- https://habrastorage.org/files/a3c/3fc/c6a/a3c3fcc6a7e448a79bbd341ae3be3a07.png

# https://habrahabr.ru/post/273535/

�����, � ������ ��� ���������� ���� ��� � � ����, ��� ��� ������. � ������ ��� Scala-������ ���������� 4 ���� � �� ��� ��� �� ������� �� �����, ��� ��� ��������. ������ � �������, ������ �� ��� ������ �� Go�. 

# Why not Go

- No code outline
- Name string `json:"name,omitempty" xml:"name"`

http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/


https://habrahabr.ru/company/jugru/blog/352438/
������
- Java ���������� ��� �����, � �������� ���������� ���� � ���� ���������� ������� ������. ������� ��� ������� �������:
- �� ������� ���������

https://stackoverflow.com/questions/46356345/can-java-9-run-on-a-32-bit-os
Sorry, but we have no plans to ship 32-bit builds of JDK 9. We�re trying to focus more on the future than the past.
Yes, you can build your own 32-bit JDK 9 binaries.

Update 2: Apparently Oracle has decided to eliminate support for x86 Java forever.

## Habr

https://habrahabr.ru/company/piter/blog/304040/

1) Service discovery.
client side? server side? ��� � Go � �������� ������������ ��� ��� ����? � ������ ������� ��� ���������� � �����������? � ������, ������� ���������� � ���������� �������� ���������� ��� ��������?
�������� ���� ��� ����� ������������ �������� ��� Consul ��� Eureka.

2) Circuit breaker
��� ��� ��� ������ ������������ � �������� �� 1000 ������ ������ 5. ��-�� ����� ��� �������, ������� �� ���� �������� ���� �������� ������. ���� �� ������� ��������� ��������� ��� go � ���� ������? (Hystrix � ��������� ������)

3) ����� ������� CRUD over REST, � ����������, � �������� ���������.
���� �� ������� � ����������� �������� ���������� ��� Go ��� ��� ����?

4) OAuth � ����������. ��������� ������ �������� �� Go endpoint-� ����������� � ��������������?

5) Tracebility. ���� �� ����������� *������* ��������� ��� ������� ����� ������� ������ ������? ���, ����� ��� ������ ������������ UUID correlationID � ���������� ��� ���� �������?

6) �����������. Stdout, ������� �����, � ��� ������ ������� ���������� � ELK?



# Links
- Why we switched from Python to Go https://getstream.io/blog/switched-python-go/
- https://codeburst.io/passing-go-for-a-second-time-a346076f3bb7
- JavaScript https://medium.com/@johntucker_48673/really-appreciate-the-response-it-focused-my-attention-on-why-i-was-drawn-to-the-opinionatedness-86ac3fcbc5f6
- https://medium.freecodecamp.org/here-are-some-amazing-advantages-of-go-that-you-dont-hear-much-about-1af99de3b23a

