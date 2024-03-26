## `amazoncorretto:22-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:d54ff95917f463ad76cdc55ce5fa503487d9c4937f9b5e59ee9d061fa0cb9678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7f5fc5d861cc0fc337ccc33741c8775de51a08adc2e2300ea7037f58eab0ebc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161480885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cc7ce042ab5c73e2b9ed9809793fd63046680b7bdbc9975d09d8d53df9b791`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 17:54:58 GMT
ARG version=22.0.0.37.1
# Tue, 26 Mar 2024 17:55:04 GMT
# ARGS: version=22.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Tue, 26 Mar 2024 17:55:05 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 17:55:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 26 Mar 2024 17:55:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f26ffcfd533d7d26c2cea440230c1b7fb2a39ac7af0d659992ff27dd31991c`  
		Last Modified: Tue, 26 Mar 2024 18:00:03 GMT  
		Size: 158.1 MB (158072156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:78c09869e8b93a4e9c04a0d4d38feb58e1930b80e417ed2b970830eafc8093cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158760169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f294581b56a930c237e952368ec45a20377e4dcc8d333d98d6c8695a440d28cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 18:07:45 GMT
ARG version=22.0.0.37.1
# Tue, 26 Mar 2024 18:07:50 GMT
# ARGS: version=22.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Tue, 26 Mar 2024 18:07:51 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 18:07:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 26 Mar 2024 18:07:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c31476814a0678b1b692fa111fbd66ec42169cc48ed4028175c01d3c133d5`  
		Last Modified: Tue, 26 Mar 2024 18:12:49 GMT  
		Size: 155.4 MB (155412454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
