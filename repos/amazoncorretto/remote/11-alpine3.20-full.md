## `amazoncorretto:11-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:2d6e8423a2577e48ac14a8ef6eff1e1949989e24546aaf023c10b256ecd5fa9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5cf8afa04d32804ab5122a932215b17dffb7dd7921a6ded9826969d0202b236d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145538649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12a91e868146eaf07145de0af7f3ceb4c9013556b3a4fd4c6ca7f3644359f77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca9254609025b1114ba67a28f9fbb47cde5e1840bbc65ff9d2fc9e9980ad0af`  
		Last Modified: Sat, 15 Feb 2025 00:03:43 GMT  
		Size: 141.9 MB (141911752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a12308250152058e900a9110eada08a89f6c2ba9c7e85c95f440de32f5c4fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 KB (392880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f3f4f7aba512d53650e167812645810d150627733dfc91a7ec70143d06c2b8`

```dockerfile
```

-	Layers:
	-	`sha256:1b28b92a44be654b582c4cc39c148cafd2c1e3512a714f9f02fc5431b2348d14`  
		Last Modified: Fri, 14 Feb 2025 22:47:36 GMT  
		Size: 383.5 KB (383463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2c1e003fe85a41c5232f11705061c48e98cd826b4bf1ffc764ff7aefe84318`  
		Last Modified: Fri, 14 Feb 2025 22:47:36 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8be02e561b719e18074fda3926ece02945a02409503815a7863dec116fc62e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144125985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fda89da8b871a3e1352c8c82442cec541d5664a52694898eeeee31563ec9ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f1dbc5b487ddd138799e7ad6976476cfdbb7dc02e25c0c3078775ad516425`  
		Last Modified: Sun, 16 Feb 2025 15:08:44 GMT  
		Size: 140.0 MB (140034820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa859f406d2353685ef0aa78417cc83e4486defeba21c871df16342b7251c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.0 KB (393039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28513b754731a722b69bc68364ffca884ddc8564b0514a2819a95dffee551cb`

```dockerfile
```

-	Layers:
	-	`sha256:1778d012cdcc934c0cc589a27b131b80e2e144e84055a3b06461e34e1925de42`  
		Last Modified: Sat, 15 Feb 2025 01:47:37 GMT  
		Size: 383.5 KB (383519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4956d35f5a3796d6561aea45b3380732b58b6d13c16fb04e09dcd5f2da3f21d`  
		Last Modified: Sat, 15 Feb 2025 01:47:37 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
