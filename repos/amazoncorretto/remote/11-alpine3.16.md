## `amazoncorretto:11-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:b07d19caf2a39475135d72e667b231644c245d8155e4e9d01cda49b4c33ab6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e899972173b5e8fb9d4fd359304e67fbb02d3a2f3e069a4cb10708e174dc6ab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197990285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea211647a1bd217ab1d00a2d5f242ed341cd1fab51e2698309346be1da4d3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:23:09 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 18:23:15 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 18:23:15 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:23:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:23:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15818f3b44ab811b7fbde5522d52f7e9485d6613f1667fef843a5b83d42069d4`  
		Last Modified: Thu, 20 Apr 2023 18:33:34 GMT  
		Size: 195.2 MB (195182482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:124141369f8a8946b695f5c30028bdd0fc6a5d89057d26709793bbbbd7a2b82f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196177982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb56ea7c8c9b9917bde58e1fbb5a69b210eb3a6c69f02de95bb84a7879e3556`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:42:27 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 17:42:32 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 17:42:34 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:42:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 17:42:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104e55ee7357c11e519813dc6d505e10f98542b1db5f2dd6539679256c46ddf`  
		Last Modified: Thu, 20 Apr 2023 17:52:15 GMT  
		Size: 193.5 MB (193468638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
