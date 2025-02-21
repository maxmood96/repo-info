## `amazoncorretto:11-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:75e1a776818abb2b19ceda288124b737bbc1f1b30fcf1767b843e2df24522d0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:592a76eca73d9ba581354117317c95a758d579dd2f086f9609520d6acc10d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145329413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f9107076198833009698eff9b3ff3cf2e92429117fb90e5d7ab8b840b34b7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067b86d4bb7cb852f7e8877607502fba73736bce19d7e944edb8cbe87c34f453`  
		Last Modified: Fri, 14 Feb 2025 19:12:38 GMT  
		Size: 141.9 MB (141911004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0a074bb63d8b56d2fce2a6fe63f5ec866c3dce6cf583262dae540d1294fa6250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 KB (396450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638e159c0724daa0c09668ea7acaf20d65886ff2a7267e276e1ba8eae6e3e6e2`

```dockerfile
```

-	Layers:
	-	`sha256:b117ff72ddd4d6bbc3b00a2b553577ec07716f67b31ecfc5958209d52aeb00ba`  
		Last Modified: Fri, 14 Feb 2025 19:12:36 GMT  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aba7b98d6466af5d3322f5b142f12c3a1ab9fe08e3643ad514406cc143ff7a`  
		Last Modified: Fri, 14 Feb 2025 19:12:36 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5cfcb646ae2d2f25804559e6389c4e09d8e21c62f2b95433063d7eff27286929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143377826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72280dedfff1e529e1bab44cb9bb0b43d0b73525490229a9dfc3e98cebe69ad1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c878e1a9a9b11290da34671cf3e6dc910ddae1cb25a098e072bd39ac13f2f1`  
		Last Modified: Fri, 14 Feb 2025 22:34:13 GMT  
		Size: 140.0 MB (140035169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b89b9e4ec2fea538e7628cb77d3930d5e0e9ca3272837db2502767d7c84f1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00d54ebed7aee8fb5232b9b7c8c08e51583e42ee9feb9536c5536bef839c9d1`

```dockerfile
```

-	Layers:
	-	`sha256:387a1301df48a2526d4dfa5908c970a160456d8dff68131cac83478118397808`  
		Last Modified: Fri, 14 Feb 2025 22:34:10 GMT  
		Size: 387.1 KB (387090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5e05681a0544751b506eb8ffcf032a9a519a99e6aa3856d5175a9d9be4fb55`  
		Last Modified: Fri, 14 Feb 2025 22:34:09 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
