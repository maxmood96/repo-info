## `amazoncorretto:8-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:b16c9e5cab2009b11f7eb29e12b788a2046935d1e08a75fd99ac94cb6a7e5cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62a6c937f81e83ad95dbbaacca9252ddd3cb0e626a1596fb63d129f9e0a8d00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103589451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acb5c2c6fbe7c501060fd94bc11aeca2d5aaf0bc00ee5da7cf03c5b44e1e522`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a06771bad819cdc40834bae0431f87cb2c3c4f36c24daf486ce8f7f201681d`  
		Last Modified: Tue, 12 Nov 2024 02:11:52 GMT  
		Size: 100.2 MB (100197199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b51388676ba26018d37180e15e090d91308562171a8eecbac953a4d09050bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 KB (254021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbf1e8782e0f6f43997712279d667a895eb75c6440481520d345e9f9460dac`

```dockerfile
```

-	Layers:
	-	`sha256:cc80ab3bccfa341062d29543e1d1fa387393ab271c5777639be69bfdfb4c0749`  
		Last Modified: Tue, 12 Nov 2024 02:11:49 GMT  
		Size: 244.6 KB (244623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fcb3f262b88e2c5d84e5d134365f4055badb3779e4240719364e9dc64515ab3`  
		Last Modified: Tue, 12 Nov 2024 02:11:49 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6205c6c64f2dd33c68db2c3022a42cde8beca5073788c3aca78ba17bde63a29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103253965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5946f7fa0733da9ef7973e07dec3c7e7acfbeb54875a8b394d0514089844ffef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8cde40339a8e86ccabf163a25fda4db5a12970751b093d2452f57d74653b5`  
		Last Modified: Wed, 16 Oct 2024 22:02:02 GMT  
		Size: 100.0 MB (99978893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5287914e60ead956c13a661f6344b6d718ec8012ebbbb29044551400aae8fd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 KB (253950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba990060145d0c4d6bc364e0e474b3998c0e7510b95aa14e45ffc6d52fe969b`

```dockerfile
```

-	Layers:
	-	`sha256:380c764d417b67eb5aabe41fb2325a257bcf9f58a0f6145df63c0306c0a26867`  
		Last Modified: Wed, 16 Oct 2024 22:01:55 GMT  
		Size: 244.7 KB (244662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7b113e96ee9382c289186a62cc2eab490b1c46d5c726a18ec73270337fb330`  
		Last Modified: Wed, 16 Oct 2024 22:01:54 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json
