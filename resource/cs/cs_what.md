## 算法
1. 可逆  （对称 vs 非对称）
2. 不可逆（哈希）

## 哈希
散列函数（英语：Hash function）又称散列算法、哈希函数，是一种从任何一种数据中创建小的数字“指纹”的方法。
> 不可逆

MD5消息摘要算法（英语：MD5 Message-Digest Algorithm），一种被广泛使用的密码散列函数，可以产生出一个128位（16个字符(BYTES)）的散列值（hash value），用于确保信息传输完整一致。MD5由美国密码学家罗纳德·李维斯特（Ronald Linn Rivest）设计，于1992年公开，用以取代MD4算法。
> 常见的md5算法就是hash算法的一种

SHA-1（英语：Secure Hash Algorithm 1，中文名：安全散列算法1）是一种密码散列函数，美国国家安全局设计。SHA-1可以生成一个被称为消息摘要的160位（20字节）散列值，散列值通常的呈现形式为40个十六进制数。
> SHA 代表 Secure Hash Algorithm， 也是hash算法一种

## 对称加密
对称密钥算法（英语：Symmetric-key algorithm）又称为对称加密、私钥加密、共享密钥加密，是密码学中的一类加密算法。这类算法在加密和解密时使用相同的密钥，或是使用两个可以简单地相互推算的密钥。事实上，这组密钥成为在两个或多个成员间的共同秘密，以便维持专属的通信联系。与公开密钥加密相比，要求双方获取相同的密钥是对称密钥加密的主要缺点之一。  

常见的对称加密算法有AES、ChaCha20、3DES、Salsa20、DES、Blowfish、IDEA、RC5、RC6、Camellia。

## 非对称加密
公开密钥密码学（英语：Public-key cryptography）也称非对称式密码学（英语：Asymmetric cryptography）是密码学的一种算法，它需要两个密钥，一个是公开密钥，另一个是私有密钥；  

公钥用作加密，私钥则用作解密。使用公钥把明文加密后所得的密文，只能用相对应的私钥才能解密并得到原本的明文，最初用来加密的公钥不能用作解密。由于加密和解密需要两个不同的密钥，故被称为非对称加密；  

> RSA算法是常见的非对称加密算法之一

## 哈希表
散列表（Hash table，也叫哈希表），是根据键（Key）而直接访问在内存储存位置的数据结构。也就是说，它通过计算出一个键值的函数，将所需查询的数据映射到表中一个位置来让人访问，这加快了查找速度。这个映射函数称做散列函数，存放记录的数组称做散列表。


常见解决哈希表冲突  
1. 再散列法  
把散列后的结果再进行散列，直到找到一个不冲突的地址

2. 线性探测  
顺序查看表中下一单元，直到找出一个空单元或查遍全表  

![hashtable](https://static.coderbridge.com/img/techbridge/images/kdchang/hash-table-collision.png)

3. 链地址法  
![hashtable](https://static.coderbridge.com/img/techbridge/images/kdchang/hash-table-chaining.png)

4. 建立公共溢出区  
将哈希表分为基本表和溢出表两部分，凡是和基本表发生冲突的元素，一律填入溢出表