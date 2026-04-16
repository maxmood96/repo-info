## `sapmachine:21-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:881ef5b65a3e049dec93aa9c33f599a2fe074028c770f700b811abc3e87ef4a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:bab7af1fbec6fe4591151812c0a0de735b4f2b790c7afd0e0f85c805109ce9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90475464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee290e1e44f288d764225a4e59ae05c62863e0c44122a9a4562ed3f168f72740`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:59:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8690c9b1210e60d695e981f2343603ccf1506c2e1965c4955c9d8480e68880`  
		Last Modified: Wed, 15 Apr 2026 20:59:22 GMT  
		Size: 60.7 MB (60742486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4dd2149d6691836c07d026b9fca2e3fe4be1790d1c17ce7694bbeeb2e014876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2642bd4de8192652854e05c6739440711bdc58c7e813b0e5a3d0559c7b2671`

```dockerfile
```

-	Layers:
	-	`sha256:07cb19900c1e8f2ab5dd13ce5eda47c812e4ee6ec4c9839e393f98f938d3cda6`  
		Last Modified: Wed, 15 Apr 2026 20:59:20 GMT  
		Size: 2.5 MB (2521108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1209c11f0a4a27b259168596c40a9be4214ba5aa9079c4face8304958d4635`  
		Last Modified: Wed, 15 Apr 2026 20:59:20 GMT  
		Size: 10.1 KB (10084 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ce1a89d90228081050df46094f89364d47a38b6772f4e751da049935b902276f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88809735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bccebd26285c36aea8fe922210e93ce8fb1110195e4f95174fa202256b1fd7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:09:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:09:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:09:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8be63f9b5c41391762f3efa71ca043c8a23a4b9d16acd5aa3dd6d8442cc219`  
		Last Modified: Wed, 15 Apr 2026 21:09:23 GMT  
		Size: 59.9 MB (59933950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92c9cad0d7434d37eafaec40250f18839d214bfbc86643995247b998260a93e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4520ca22972eaf2f362ae9e73a0243c80267c0d57c09bbac618bef4bde8e13`

```dockerfile
```

-	Layers:
	-	`sha256:92b4a7826457205c83977f0959cffdd3eb3cf8bbe278a218dd65306897b977a0`  
		Last Modified: Wed, 15 Apr 2026 21:09:21 GMT  
		Size: 2.5 MB (2521624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8396d6b1a726ea5719878b27826c953fee9927210ffb565db87957d927bb9e`  
		Last Modified: Wed, 15 Apr 2026 21:09:21 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:371e3d8214de6880e819ebc464f9c0f4dee0dfcadb89fcf0dc6d3aa6e12e6e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96359809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70406883ad0cd0009ae077796bfca9d788bd1e493d1ba7a6e1ec4fb9b54a4c6a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:07:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:07:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 09:07:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191548f38f7dd9b10bd6d54674be16e183e8c14352c16d135ad974992d3453df`  
		Last Modified: Tue, 07 Apr 2026 09:08:25 GMT  
		Size: 62.0 MB (62046475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bca8b73bd5656973aa5b080edc9cf74484c75dd1ea6c83328eae4f1c30561ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f45ae2b1dd5117e3ecf12afdc6a99359b8948d85b9bf266696c85f806b6720`

```dockerfile
```

-	Layers:
	-	`sha256:ba2ab9d9d4b7ce869f7865220be6624f0cf62b2d81395094cb46882bfdb6e1ce`  
		Last Modified: Tue, 07 Apr 2026 09:08:23 GMT  
		Size: 2.5 MB (2520606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47c2859b5e3526f0d955c3b9464280bd5c13f4bd38ef08f14ca39c0fcac8656`  
		Last Modified: Tue, 07 Apr 2026 09:08:23 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json
