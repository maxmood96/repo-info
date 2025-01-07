## `amazoncorretto:23-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:b7ceb3b1863f436c5c3aa932a0f6891b0b33fc3ecbd108a60a7b6e2b82c0ab41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:64ff0ca1ffa352fc15fc97de8a644629b041553deef4cbd826acca8d8a42957d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170074933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac1f26583bf96d85e07069c703a6404a2366304a7912583fe181a84d9aeabf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195387818aaf6c946d164151b31daeba708b5d1103fac930ca8aca3106387e15`  
		Last Modified: Tue, 12 Nov 2024 02:13:17 GMT  
		Size: 166.7 MB (166658532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c38adf7f7bb322b90605d4a9c768c2ccee742a747e5088ee2dd637aebe3a403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37888d639bbf3127cb6dca9b70d5e0465bd6794051f61eb4654559c3b17dafc9`

```dockerfile
```

-	Layers:
	-	`sha256:79960cca74ceb1cfb016fedf402ba2e7206f7795e88b411f6444a06757d5b352`  
		Last Modified: Tue, 12 Nov 2024 02:13:12 GMT  
		Size: 382.7 KB (382709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb3511adfbe23ec9f97ac384eabf12016f813611f96ec649f701884786494b3`  
		Last Modified: Tue, 12 Nov 2024 02:13:11 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a617284f796b763251404cde794bb69cca987d15e0cb5e84d2fef7ebd478ad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167693647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74f321044a45a87ba6fd3eacf440c7d2e03d6701125b9ab7c3a92afe3b1b8a0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93694739def933a22f6c0e61f3a241d142e3694de89d5389d5656a99c4fb09ec`  
		Size: 164.4 MB (164353196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fa27110bf21842a99849d03ec3f0f8c1c64ce5dc09ef5030a98b52449515c2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 KB (391004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b023331c58ce88e4dc4337893267996a7082a2d4b8633046611fce02a176c`

```dockerfile
```

-	Layers:
	-	`sha256:bebbd7da72bb1a0658e0540ec61cd0f10845b3d024808578cdd490304c43a801`  
		Last Modified: Tue, 12 Nov 2024 11:14:12 GMT  
		Size: 381.5 KB (381486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350056ab62f4aa1fbb5a03dc9ef322aadac03c09c3ad227e324fb49de3f40539`  
		Last Modified: Tue, 12 Nov 2024 11:14:12 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
