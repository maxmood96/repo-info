## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:2d266f6648248a09e345532366b357d706627f51fda8be5a7ba52945b3d1f6a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

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

### `sapmachine:21-jre` - unknown; unknown

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

### `sapmachine:21-jre` - linux; arm64 variant v8

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

### `sapmachine:21-jre` - unknown; unknown

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

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:52f83a5baf9ee503b6f33732c3c31f1cf2fc69e376c972a512be39ad71a46dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96360712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe4821299b2b34ce3becad5dd6bae96265cff52a077b420c9bad36b9af6b75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:34:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:34:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 23:34:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088e3f91890656e7929de4a72ae23ab4de1c0ca44df22b2919f6ec9d255f9bc`  
		Last Modified: Wed, 15 Apr 2026 23:34:49 GMT  
		Size: 62.0 MB (62046534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c0e2edfefa52d13dc6bd77ce1d0e887bca5443c5062b249d6722578ca55fc718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d0b3ee49778019f0086bf7be72d472610b79dd3af8be62c6d885c3f0a32cc2`

```dockerfile
```

-	Layers:
	-	`sha256:6364897f33ff220769248a7f50cff981899e7d5bc930bcd2077fc1ea32a21767`  
		Last Modified: Wed, 15 Apr 2026 23:34:47 GMT  
		Size: 2.5 MB (2520606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd47070fbde971e8da421d4bb7fd68419f6df73578811619bdd2980a64a1ffab`  
		Last Modified: Wed, 15 Apr 2026 23:34:47 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json
