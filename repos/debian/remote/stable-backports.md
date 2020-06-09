## `debian:stable-backports`

```console
$ docker pull debian@sha256:7f39909306e5c6115a9a86360c7772e1395290b3e22ceba3409820079be27f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:45b053ff90db99b1403e3aaee65bb1f3b8c57bbcfee44ea3285e1e89f0c3190f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50389733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049fd63ee7da354640ee45a11dead51994d5a29c1231ef4fae8fc98084cf216d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:53 GMT
ADD file:d0a040d1c2c2348f6bec0a2c1cef74c96e2fe95c2a3c73d685faebe531a14a6b in / 
# Tue, 09 Jun 2020 01:22:53 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:22:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:baa6dfcc50ab53f3455ddb00cf84a4943b6539a0c9da6996f22ee74ba987f9a5`  
		Last Modified: Tue, 09 Jun 2020 01:27:36 GMT  
		Size: 50.4 MB (50389514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1951a3ef8c30e781ed721479887804330caa499d825b4cc2f8e499bff5a9f79`  
		Last Modified: Tue, 09 Jun 2020 01:27:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9f6169efc76bc19fad57f3504d18e70fdb3cc39c9b298019f68a81657d6d3e82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8e54773f67202ac3c7cae4fec7d0eb3710d20a9aa3f5f6250a43127b46c1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:54:44 GMT
ADD file:0026f1e193f0a9d56dd3032b1ccbf3b8d6f5ae0fd5fd840fa7d7f93d419726d2 in / 
# Tue, 09 Jun 2020 00:54:46 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 00:54:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8140e0acb6af8f7405fc6ea79186525c638fab1147cf473227dc8ebd3e1b7e26`  
		Last Modified: Tue, 09 Jun 2020 01:02:14 GMT  
		Size: 48.1 MB (48107109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bef53054c32dacc6f312a7a438a6fb6e68d4f53096859fdfa084594f8cdfb87`  
		Last Modified: Tue, 09 Jun 2020 01:02:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e91b08ece94045311477005487d4e4830cfe1142f73abeef93fd03258add1012
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45869216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da81a9428f440ceb0aed874fcd676efe3ad795fad94622c4768a66eeaba67a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:05:11 GMT
ADD file:3eaec0239cd9203afd3f340f502aec2627ea565c273cab537d6bfac593a19e90 in / 
# Tue, 09 Jun 2020 01:05:14 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:05:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8889795e1736511f2efd9d53e914d9ac0ded34e7ca7ed10c92d808a60bfe7f75`  
		Last Modified: Tue, 09 Jun 2020 01:13:02 GMT  
		Size: 45.9 MB (45868992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32252e4887f9cd2e199b56dc97db770043a20a39bc1a371ae07367c90bc2c2f9`  
		Last Modified: Tue, 09 Jun 2020 01:13:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3ec58909d1fe876795e16d0f041e5de8b98fdfa5e19a14719346455ba7a0bf7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49168083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978f15d9fd1127da802d125e8a7dfd820369098054d5ed8ebfd6904a7ac269dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:53:41 GMT
ADD file:5e0d5c9cefbbc48abd01ca23c5562a554219a803d4ec8efb097929d189d99971 in / 
# Tue, 09 Jun 2020 01:53:43 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:53:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d455859f019309753a154f2a692a596b239a5887ceeefaf9eda5371f9054c1a`  
		Last Modified: Tue, 09 Jun 2020 01:59:36 GMT  
		Size: 49.2 MB (49167859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381dc91aece242d543605807e3e4ab73e75bc5faded2d6e424a0c55ea7285dfd`  
		Last Modified: Tue, 09 Jun 2020 01:59:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:e797033eb8c01404dfbd50d27b571b47d65853395232bcd7678ba591eddbdeba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51156413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd1f3af943cbe6d0b83d493d667230a4a455183e307e6ccf625d6d2b0089591`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:41:49 GMT
ADD file:f665bb1fec8a2e521aa1e0a1c67f19270477a23597057dd7fc1492275d6638ce in / 
# Tue, 09 Jun 2020 01:41:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:41:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8541ceb6873ad88a62277b5262eeb2a2cfdc55e1bb56b8ec663ccc8f90bf6579`  
		Last Modified: Tue, 09 Jun 2020 01:47:40 GMT  
		Size: 51.2 MB (51156190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1810bc954d10f80816300f6a869fe368c28da9edc6107441eb8568844b1906f8`  
		Last Modified: Tue, 09 Jun 2020 01:47:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eddc575b152708f1f1c03284976f28ad7d5357dbc794163807552812f0ff6765
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49020061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6dad8b130f8d078c4608122e0678cc2909e5ebe0efb4a6e083360d38d8e2e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:12:01 GMT
ADD file:eb9f0378bdb3ee9ed716c79e85d2f3fbeaf59aa3920bd57bbf7a34c68f35e4f9 in / 
# Tue, 09 Jun 2020 01:12:02 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:12:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:080716cff6f1ffa165db896d43334675c0c882a3c4f2947374bf8be21cb50998`  
		Last Modified: Tue, 09 Jun 2020 01:21:34 GMT  
		Size: 49.0 MB (49019837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784aa4182d8b376e40a507dba5041a3b88039a53584a0559eacbcd199deb6f28`  
		Last Modified: Tue, 09 Jun 2020 01:21:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ba699c900a8eec4f68317894be7ccde05391460b2344a2dea2e682cfd90014c3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54143571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2819f23d53f4eb4cf797631a9d24f129490cfe848c9af96a5a707b9e4ac1c40d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:24:24 GMT
ADD file:abc456eb96e450d5cb22ae2f7c4460611b08f85c9330a356471b0ea8f044aa79 in / 
# Tue, 09 Jun 2020 01:24:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:24:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2fcd8ce49cba897cab451e1620072aa9f85506fdb0a56326dc4b6c919560be7`  
		Last Modified: Tue, 09 Jun 2020 01:35:16 GMT  
		Size: 54.1 MB (54143347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831e748262469682dddb416c856d75dd50d7cba5dfeb2d1770d9872134f86387`  
		Last Modified: Tue, 09 Jun 2020 01:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5fe5ec883ffb03dfb38bc49954b41035c6df24ecaed6cc421fe8d205f39aeaba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48966110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c75b81c43fe5b017397a5c5051414fe25941cfb859dca2b3a0c580662a0e552`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:43:37 GMT
ADD file:52a9265838917b1e17fda43d3300eb7e275baaf0eb48000803a2a01b9adf4349 in / 
# Tue, 09 Jun 2020 01:43:40 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:43:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad1fd55c73f07628bb6037e5769087927cb50cb9f73988b69baee4ece47bb234`  
		Last Modified: Tue, 09 Jun 2020 01:47:27 GMT  
		Size: 49.0 MB (48965888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b66b82a77b46d2458b6c10db96b4421f00ac2def21dda7217b28885c7ce4dc`  
		Last Modified: Tue, 09 Jun 2020 01:47:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
