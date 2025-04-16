## `amazoncorretto:17-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:0c85c24271584fa4d5769771e777869a8440b5a63863093277b8cf6a6e8f6ddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8350faeed47bff297e8692f5a1bf35a427271bbe7ea30090c00cc2f41b83790c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149172769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d82b758866d7447db84d9839d0d212e61253d8f5f7f0c99c70a6d0cac5a11`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d35b9d2bc0647974123b8907d47c13122c573a97b743802ee8e0e6690ae0`  
		Last Modified: Tue, 15 Apr 2025 23:55:40 GMT  
		Size: 145.8 MB (145751901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9a3b80a12874ad04eae3287c7f7e1eed7f06446939f6e871e5dd410eb012f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ee2f4cc02de75948fc86baf5499ecd27fbe55a76101aea6274a0da2d8fd8b9`

```dockerfile
```

-	Layers:
	-	`sha256:f4addf899e6080da6a19ecce53cab5b33b52084f21549c5471e51ef5709ab5cd`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 380.9 KB (380893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa02a5e64e48ba55846de3af4f9251fa80f8271590615180781c6a8f0fa4380`  
		Last Modified: Tue, 15 Apr 2025 23:55:37 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5c93b20d11142d9624f274afe53d66535d82fecc98ea7660415e2d24530063f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147383041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f82bce4c314485e6ae1ecc6aeeeaa9f35906c50d8cc72e97da8d223a50c6ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:89fc6283640d139ccc434ec625a8e84a075276e38c697b6e5ef88b4eab140ede`  
		Last Modified: Fri, 14 Feb 2025 22:36:38 GMT  
		Size: 144.0 MB (144021617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e22825776f7bc04046008ad0faf2585b9d0aa1cf21fdf7bf86cf1d311620d0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b62f4ed1109773f1a86f070f8660d6f633909f35b000a8826e4ee5f8658b56`

```dockerfile
```

-	Layers:
	-	`sha256:0c6de7e83453c7a7636bbe1b23108e167f0cb8c890acb6b0cceac97fd3e73f65`  
		Last Modified: Fri, 14 Feb 2025 22:36:35 GMT  
		Size: 380.3 KB (380312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1984695abc1f70df5b23962ab0586f8099b52f5f1f2e08392fe70cc0140ed675`  
		Last Modified: Fri, 14 Feb 2025 22:36:35 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
