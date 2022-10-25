## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:c33f15153b1616d192ba96b1046b844379b5c74244542d799787e480cb11a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:cc966d558163b2c444e75b9f98f82b9ff3937ebb3197e77783e9e929bc373136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50447986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524292ee0b4e17fa1f18838b052d0c780295ce929da220ec105ceda9703913b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:21 GMT
ADD file:326adf2063d8d292211a8c3f1b0ed03faeac6ac47a2bf31c02c22df04e81a3eb in / 
# Tue, 25 Oct 2022 01:44:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:44:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c3cab76daeb46f383600922bdc00d7e2095afa471338147c1901af943ba4792`  
		Last Modified: Tue, 25 Oct 2022 01:49:00 GMT  
		Size: 50.4 MB (50447761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e60dc9add3193c2ae715a89e232822346e2a800d7cd75e237f4fc26fe4bbd`  
		Last Modified: Tue, 25 Oct 2022 01:49:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:05ecd52738c6b9dd9c8360511c0266b2f9ed5fc4b17af20843c98b8628a22640
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823d472049dfc91e28ec77cc3ac0c4c55d6a5be8ed4713fb2dde83abbd697d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:12 GMT
ADD file:c4b78f22401af0cad6ac70191492b42eb3613516a46b123ec64b9ab0c81b4ee5 in / 
# Tue, 25 Oct 2022 03:15:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:facb5eefe2e92765f79b56f7e31fbb17246a13cbe4916b33b6774f27283c88f0`  
		Last Modified: Tue, 25 Oct 2022 03:22:38 GMT  
		Size: 45.9 MB (45916221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04640bc18d5d0c26cd11a3732560cc0777ba902b5c9753925c970590b772b4ce`  
		Last Modified: Tue, 25 Oct 2022 03:22:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c2f77ffb3e3211da92610c80610fde0b287bf431ea634a3953040977fa3eda46
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49233501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a621c71a2dc986b84c0370348bba3f41940663cc4d07d605dc8942eb1432174`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:19 GMT
ADD file:2cda1bf8dbd2fcc1abaae846fba594b3596240dbd8a790043ba7fbf889bb8870 in / 
# Tue, 25 Oct 2022 05:46:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:46:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:002ec38680af0eac962657c08930ab401cf87749e9afefa3ef85f3b2e0709ead`  
		Last Modified: Tue, 25 Oct 2022 05:50:05 GMT  
		Size: 49.2 MB (49233279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ad61fb18ffe18e6598bc357196e81c860c2c045b2483cec35d3a4f3869144`  
		Last Modified: Tue, 25 Oct 2022 05:50:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5ac61557f86a69cae923e07bde5505b6f588e2ce8220fbf45be628b3b6c65479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51208184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1c248c6deb5ad42b81fde402ec2c9ad5c6228ea920b42569c0730b6bb66f24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:13 GMT
ADD file:4308a4e31a597a68a869ed89293f56effa688d73fd2ef1f42b2167991e9191ea in / 
# Tue, 25 Oct 2022 02:23:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:23:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1231a6244b56ad7b565bc454e1b6fb5c2945c1fa6d068d84483a508b2b20323`  
		Last Modified: Tue, 25 Oct 2022 02:29:41 GMT  
		Size: 51.2 MB (51207960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f379a5647c098ad3f5dc76518eba3bffefb41e46e8a4597b6280627158f5d`  
		Last Modified: Tue, 25 Oct 2022 02:29:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
