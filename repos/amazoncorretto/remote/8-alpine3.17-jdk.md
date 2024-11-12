## `amazoncorretto:8-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:6240c9b67d754a7f199710b908fd2b3b20caa7170709b7193a2c2e5a0d23a2e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jdk` - linux; amd64

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

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

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

### `amazoncorretto:8-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3f4f8854f7bf920fbb2d862cc7997149aad79d6a2122c077a32063a3a5990efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103254200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdecbc6493feba8ad203e84e7897a550e3d01cd4df7d5ed27f0cba699c053fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa65a1653dc59200f7c4a89dcf15c2b02c6717b56a2dd42a120e757632739f`  
		Last Modified: Tue, 12 Nov 2024 11:02:19 GMT  
		Size: 100.0 MB (99979039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c9bd1edefb84940ba60e5ce30f8d367b357f7eee099f877ed7a6a60c88e6a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 KB (254254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5d2c6a10b42d52de441c76d3e2573e3f8d97e99a0430a09b52e1f11cccce02`

```dockerfile
```

-	Layers:
	-	`sha256:9f1027fe7249097cb0901bbc067327b9ebea972f8407366e40acca6c0a6793ea`  
		Last Modified: Tue, 12 Nov 2024 11:02:16 GMT  
		Size: 244.8 KB (244755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84873c86bf72abe816754b24fdf0d8ef50db62d22630549307ac7c5a14c381b8`  
		Last Modified: Tue, 12 Nov 2024 11:02:16 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.in-toto+json
