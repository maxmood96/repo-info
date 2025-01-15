## `amazoncorretto:11-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:0a1d3134c751c5f9f36afd04192149119bb72b8c08261278d5be9d6192ef1642
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:65344443e0251e4e1c2bbfac6e9f90d681034bee97540fc3d95bc7d3021ee5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145328203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5d8c8b6f7111884a2fd29ff30b8b539e0356b0743c8594532dc5eb52fefb3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182629fdaf3f2b71497c27fcfccc85f32815e9ec473ce834f59e999b9f7463fe`  
		Last Modified: Tue, 14 Jan 2025 22:52:57 GMT  
		Size: 141.9 MB (141910229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:941794684c080af86d872efc6c53ee16f2f4737c9d34b440820103fc547f6537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0671585c8b996bfb7859e1bbc9d40a9d47da70205c625b39469d6b63e892dc45`

```dockerfile
```

-	Layers:
	-	`sha256:22430efd00cb58509f0f6129d2c6229704a0ff5d80ed2b8787fba1b4889d8cb3`  
		Last Modified: Wed, 08 Jan 2025 18:10:12 GMT  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0ace9d136757f1b57dc5555a9cee285141ab0aa6e324ec308af47b695e2341`  
		Last Modified: Wed, 08 Jan 2025 18:10:12 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:159c6065383f032e08e27335efc4172d83982e4ace2f0f638b18d96387340325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143372855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000fb630e0e0ff8e29686615bd5cd0ea87b292c5fd122d998de2dcfa092d064e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0934a63d054479c57efd5f5dbb255f352073af0cc10182cbda7925da7622e82`  
		Last Modified: Wed, 08 Jan 2025 22:18:14 GMT  
		Size: 140.0 MB (140030994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9023957db451bef805e8cac7ed86b6dae1aa35759fec8a59621895983a90dac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a07f69c76a80778fb8f6ac82e37d0eb23b5b737a3e80275e0ad1f415a905da`

```dockerfile
```

-	Layers:
	-	`sha256:f557349ee56b9fe2a6fe05e8618a6d9a7d142ce0bd96869371c724808b0aee55`  
		Last Modified: Wed, 08 Jan 2025 22:18:11 GMT  
		Size: 387.1 KB (387090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0a431160ffec527d642b48680e0fc95d02bc438e157aad84db1542c7395013`  
		Last Modified: Wed, 08 Jan 2025 22:18:11 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
