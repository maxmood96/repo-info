## `sapmachine:11-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:643aa28bb807016b34aa33b00d5a671ed3d9801e9f5ed2704590b4cf6630793d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:af9768edca565efb98688a39f31f66b92ed5584d79ca9177ea4e3172cc40ae4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77013654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29de5d0595b6dd4fffe141f5b323cb27713128eb869df83b238242dbd1bf04ce`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0bc454fa3e6b9cb6594cce5c28fa017a6abbdea9b1cf6e7c2912342852fde`  
		Last Modified: Wed, 16 Oct 2024 16:18:10 GMT  
		Size: 49.5 MB (49502594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b7b2b9dd40a4b11141e54f64ae510750ebe7adf041fca4d30a3a24db078df62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f36d974eb1987845d69bbf9093e9ef296f2bf66971261906c08ec2215eed4c`

```dockerfile
```

-	Layers:
	-	`sha256:0324ae8b91df475f5e1f6c7789a8f14a0b3144b4818190237bf5400ad2fc9afe`  
		Last Modified: Wed, 16 Oct 2024 16:18:11 GMT  
		Size: 2.3 MB (2291720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09c1aae9b22a90a7fbdf9d4d075c49eebdaaf0dce3980bad0ed2ad9466c3948`  
		Last Modified: Wed, 16 Oct 2024 16:18:08 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dc431abf863a4109465745f23564954b2097d43af4066d6a60e7b2b56125ff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246b53f4477bc4c80c3a58bfe1a391715904f378c3d6ee888b55636a30766775`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe92357d250ed68e5f1c160bb94fb845f903609506b8f292722fc4bf1bff8e52`  
		Last Modified: Wed, 16 Oct 2024 04:53:43 GMT  
		Size: 48.8 MB (48817435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c356248ddc3c53aa50a9662cd26fed7e48cb7447ab4dcd770360a294a918a081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1078101a3be976a5f9762d6485c72719db5169228d39595194f8f32dbf2f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:2b7ef52c2e994438719ba3de2b4a6007399c3053f3aeb101390ab2c7451122e9`  
		Last Modified: Wed, 16 Oct 2024 04:53:42 GMT  
		Size: 2.3 MB (2291984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c78552edbae7b12e90305b0b91924537b13f795f58896692c99fbddfd49520b`  
		Last Modified: Wed, 16 Oct 2024 04:53:41 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:87c7cf2416dddb42f085743cfddc93439972a2ec9da0b16204f3e51b00b49727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79822287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a91f7a1c8afdf0dfece02980c773b4d17cc2ed61082a448a28852e83bdbe5b0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3c1857af0e4f94b33431b7869903688788599c86a75eb04120368fc9d5c9c`  
		Last Modified: Wed, 16 Oct 2024 06:18:47 GMT  
		Size: 47.7 MB (47745781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d5ae1046235d9090df1059829a22ce06482f85cf451089606d49c839f96ea75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a51b0f096fd0c5e7112913e8954b6ab40adf4b71ac13fbe69779889c45a633b`

```dockerfile
```

-	Layers:
	-	`sha256:c0d77733d7f7156cfd2f7788a2c8587afbf0b62dd92a4c841d63a27e3c2daaf5`  
		Last Modified: Wed, 16 Oct 2024 06:18:46 GMT  
		Size: 2.3 MB (2295491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d836ab09d219baa22fcbfe05ecb7ce647d35650a19cd293a9c71b9bdfddb0695`  
		Last Modified: Wed, 16 Oct 2024 06:18:45 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
