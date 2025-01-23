## `amazoncorretto:11-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:8428803b282e83b51621763aaa047adce932504143a402557177dcaf6447c143
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b70601b23cf59662cc16d941c14e45d1700adc9b0b4b742fc1045665c9241f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145330637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831668f5cb1f2f5317ff5c319b5d61fa21418f5d383e278b904b4ab6a83e408`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234dd1f0839ed6183e7d592e69800688a102718c04046ae02ecc4f866827466`  
		Last Modified: Wed, 08 Jan 2025 18:10:17 GMT  
		Size: 141.9 MB (141910395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0137d9baf422e90eb6c1de22e392246631b3149b2553c8e9826e8c341cafec9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2d8c3a1cf2f7277d41dc7399e241169f3fce4561daedd49cde3614b57eb64d`

```dockerfile
```

-	Layers:
	-	`sha256:cacdd67a0a37fee9582a9744876d2f84e5b158b5ff39981b2c9d51ef3ba39669`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 387.7 KB (387693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b951db44d3797885d26a3d70f7ffd4aa6dde011c17dabd2601f426e1b3c6b063`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:558caade6a6bc14ab38adf0796284eca9799441dc944561de03437379ce32946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143395417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd774f6d608362a6349179c9614c210d450d73095ffaefd914b7a765e48f23f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cebaa16c89f6b249f96b1bbbb360c4eb148bcc597be19109eb7ea74b6fc4741`  
		Last Modified: Thu, 23 Jan 2025 18:40:21 GMT  
		Size: 140.0 MB (140034885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52c57b1dba49d2d3254fae2b629d8023c43f9d2099ee27ff25f7bb4fbd64b12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 KB (397268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c07609f9a5d8750c89593641952432414da852cf1a4edd80ef1316af4292f2b`

```dockerfile
```

-	Layers:
	-	`sha256:d5ea8a624c986005c96479cf33829e05362d2248a03a802a2e3dcd68a8fae997`  
		Last Modified: Thu, 23 Jan 2025 18:40:17 GMT  
		Size: 387.7 KB (387749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f878ba04dba5eb132f133e3245a50e19418efbfe2fa56e3a7c839439e16583`  
		Last Modified: Thu, 23 Jan 2025 18:40:17 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
