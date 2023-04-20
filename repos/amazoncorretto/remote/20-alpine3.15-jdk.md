## `amazoncorretto:20-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:fffbce1bde8d8ad34a36592c79f041bc5f8c82a2dca374247d909c485ab2f460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1df5912016b428752817488bad17bc8782e0eae14ffd39aee5180ba91904218f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206451278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03b9760e07141caa0d22ecb3cde71d237f6e62ba0a95ed65164e2d190c8cdb4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:26:04 GMT
ARG version=20.0.1.9.1
# Thu, 20 Apr 2023 18:26:10 GMT
# ARGS: version=20.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Thu, 20 Apr 2023 18:26:10 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:26:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:26:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5da49f1615a6572cbef90ae833dbfaf98fb6366b4c3f5be21cf79afb38212af`  
		Last Modified: Thu, 20 Apr 2023 18:38:39 GMT  
		Size: 203.6 MB (203624682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-alpine3.15-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7538b61239136de1ca9a3ea42a204661810ab519170003dbf0ee93102514bce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204453881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24695c43b295aee19a6e6c0202311c5fdfcba85924e08241a429bfa47f55d845`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:45:18 GMT
ARG version=20.0.1.9.1
# Thu, 20 Apr 2023 17:45:24 GMT
# ARGS: version=20.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Thu, 20 Apr 2023 17:45:26 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:45:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 17:45:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6287a96de7d45edcfb0f308b9c40c2568e95bf0c0f447374274f46b39cc4033d`  
		Last Modified: Thu, 20 Apr 2023 17:57:07 GMT  
		Size: 201.7 MB (201731879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
