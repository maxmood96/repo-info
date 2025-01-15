## `amazoncorretto:8-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:45ecdc6e168b2acd1245fcf3930b0399b2d2349a9078ec9a5c26592c4c68d6c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e17d115061d7d5f5206a3338d356ab6b8475922af9fa951ff70c1c7347fd6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103617481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4100d92022c968ba3d20d04978b06f3ecbaa592049ae6a60151b7e0ef5908a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dcc628e7045df83865102b5a21f89001c7724fd2a4e8ac68451492e90c86e`  
		Last Modified: Wed, 08 Jan 2025 18:09:26 GMT  
		Size: 100.2 MB (100197239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44ede2b48a6faaf7d330db646a2ee8619319630abba8ad70179732d5a458a149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f479d95354b42ad49249a28e227f0a4f94d90ef58283269d833fd5a72875860`

```dockerfile
```

-	Layers:
	-	`sha256:fc434b0b2320f2ac96a6426b0808b9842fe5871736f3c41251b473889b21a090`  
		Last Modified: Wed, 08 Jan 2025 18:09:25 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d5d87ec5da97ab7572c50e316ee98df96020f4cccf19885336ccd35913c54c`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e94011e580dc67c839590cc6ec0ba0824a4e8e6177ae1703b71150d939d9242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103339538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77487ad2b404ac37d4fed94ffb9e61ea4f4b9fa94a231a85f3e9b2e92abbab1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78eb822fba61d9d78e3849aa76a39486bd0be886a2ecbda20ccfa2d29b848ee`  
		Last Modified: Wed, 08 Jan 2025 22:16:42 GMT  
		Size: 100.0 MB (99979006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e0b833aba9871fbf1208e66e4d05e4b427b745e7f0d762ce5b622ee18951dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be62e939abf24e6b8fd42f23b34f8b770cdf513bc636c9131a5a9d1950d0a5d8`

```dockerfile
```

-	Layers:
	-	`sha256:26840c6ebefaa54cca97cd49ab4792a53126cb883271511239054f118270f0ac`  
		Last Modified: Wed, 08 Jan 2025 22:16:40 GMT  
		Size: 245.8 KB (245764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ec7cc0c66008c8ee14a6b075663eeff3520ab105b099455fc1020121a9d93b`  
		Last Modified: Wed, 08 Jan 2025 22:16:40 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
