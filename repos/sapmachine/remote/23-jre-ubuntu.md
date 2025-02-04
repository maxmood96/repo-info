## `sapmachine:23-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:cfafa91c81fc18e104f06b6840285c3a9a89e568926ab3a4d875da9e8d6d5e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:3c47eccf314f42ba6a1c7071d17656357297e3700ab65fdebe3a37ee48976c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89914076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09093353d3057374502f1dbe725686253323295009015ba22451822a94f97a6b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292a23f8ab629ee8625a24ae99ac107102ec903b5a520f986f539a84f5b0dff`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 60.2 MB (60159786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5902377b8cf57a85a6dfcc9008092d70ea00a260125491d32a88aaa27d748317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9db616a463ff352e82e2677b570099ba66de0d31972cf689c7d0122006426d`

```dockerfile
```

-	Layers:
	-	`sha256:159804195bf70afe862690bb4614801eaffe73f3ef2294307174f41cd5f6f098`  
		Last Modified: Tue, 04 Feb 2025 04:48:16 GMT  
		Size: 2.4 MB (2391257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcad235d53c4665a9836f5b6e553d5328d2860708819f32cefe9a5c2f8905f5e`  
		Last Modified: Tue, 04 Feb 2025 04:48:16 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3dfdd599666eac5fb0b28b1a77378dbaf3c942f5ed7d5f41aef36f7702794287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88130443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef3c12d0805f1d3fdd5b34a336ef311c18a50336ded1dc75989fa36dad02e46`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9a6b84126b3ec0782a1879a1b4ec39ed1266f25f9d0dd85b58ccc331d9dd3`  
		Last Modified: Tue, 28 Jan 2025 02:22:19 GMT  
		Size: 59.2 MB (59237772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c4c396e778453a5a9327533ba957d37d17e6412667f618fd365762d95fb7a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143213663fdea70faba8a7674bcb110558a5f41f11c34e70a2046b72dd31b15c`

```dockerfile
```

-	Layers:
	-	`sha256:b674108ccac89e7e2a8b82de508c4ff82fff34c9a1ff416ca6ca0ee784796425`  
		Last Modified: Tue, 28 Jan 2025 02:22:18 GMT  
		Size: 2.4 MB (2387193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b5a5bf628ef203ad1e62ec2c172dbed35b87797b92f93acb4076d0e84e2c88`  
		Last Modified: Tue, 28 Jan 2025 02:22:17 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e6af005ceba7ab0c7f13cf0bf799385394607f9c4951d44c8098d12da2cfbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96123793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b89ba1fb36e5b357f4d97abe0569a1e9c7d1ed4e196dd984cf50c6c0dcc19d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc1206cd8c684cbea92949cf3920ed6a0abe3e6a41969f0619a3cff690dff0f`  
		Last Modified: Tue, 28 Jan 2025 02:21:50 GMT  
		Size: 61.7 MB (61734973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0056ce2816ce46a0e594bbbc086c89429757feefa8dcf974bd4c28eaf64a8f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2cd9edf47a1b79b96cb0eb5ad200028b085e9e77fa965e706ca5c5b713a9f6`

```dockerfile
```

-	Layers:
	-	`sha256:77e696e607410bae1fede7d7db24738f360ff2e12df6cae3e5cd4974d5cad4b8`  
		Last Modified: Tue, 28 Jan 2025 02:21:48 GMT  
		Size: 2.4 MB (2390634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ae7ff63013335ed4dd42ff607dc76e1a44094e95943ed7b83959ada0d230f2`  
		Last Modified: Tue, 28 Jan 2025 02:21:48 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json
