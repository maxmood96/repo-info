## `amazoncorretto:23-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:c60a85ad30262a71a6487a636a26591d1fd3af3f52abc497f5b74818ef097d39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:35af26594a4933e6e7026c83f546c1a973cfd1e1ba54644b3ed380a41e4326f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170109314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b7a6163bc22c5dff6394bcf498563cfcfdd0b4a9db5bd0ecad2a08e7d9c3bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79ab6925871b297230cdec2780f2c43ca06b50cf10ebdd0c56102a93cb3426`  
		Last Modified: Fri, 14 Feb 2025 19:13:01 GMT  
		Size: 166.7 MB (166688446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b78e392229a160f93d8d6c004e740842bbcd741abed4428a5ec825799ba6b243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fa4be952d4467c326db173b39a2e177f4ea8b8ba8c85215436acfca4599784`

```dockerfile
```

-	Layers:
	-	`sha256:2cf46a088b2653d79422e75850515da1adc70f01768aa9b3c4a7f5803d0f80ed`  
		Last Modified: Fri, 14 Feb 2025 19:12:59 GMT  
		Size: 382.7 KB (382737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f047de4b8d49c566f5bb3b6fe43f183c9e2d8de5d3c95709f01c9e34b5b0558`  
		Last Modified: Fri, 14 Feb 2025 19:12:59 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0cea71c5b91da8488476d4f0f3e1cde77f4e90deedffdf183a2facaff717161e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167770379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96151d5b78a53c67e5954e96cd7e87b9e4d2b8c7b35a2d7279b70a48b9d66345`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364d3f8fed9f5a1ff00f6506c8ab783082430e2f614561aeac59a82ada8d4c0`  
		Last Modified: Fri, 14 Feb 2025 22:40:58 GMT  
		Size: 164.4 MB (164408955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:02b5dad9ce7502d9fdcde540d355081a2f9216e56df23faaf8f7e94700751514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 KB (391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bee91cad754b911bccd790729bb27413abaec339fff04ec999d6b69f1d0d49`

```dockerfile
```

-	Layers:
	-	`sha256:d9f134df0a355cd01c1a9f1a73c79138b8fd8c07bae4a1ecdbc0eb2beaaee231`  
		Last Modified: Fri, 14 Feb 2025 22:40:53 GMT  
		Size: 381.5 KB (381516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339b81ebf7db80822977180f107ee5908924cba2609db361a3daae25f4069c09`  
		Last Modified: Fri, 14 Feb 2025 22:40:53 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
