## `sapmachine:24-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:4da1fd91380af0fbcfd3811189349da5cc63cc0c3cccc7d55c4f314643f4062a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2d5d9d5d4d090a3272eff817f16f25c338d7eccc0a4d498007524d7e5ba7ce8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260939202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc18c5582f3a29549e219aa407af524738bb67faab5a421aa7b42670987e0693`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9abe8382509dfe8f9aa874c29f43898e3a097c02e6815bac402844f2a58f`  
		Last Modified: Wed, 09 Apr 2025 01:20:45 GMT  
		Size: 231.2 MB (231221550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b407b66920374d1dc6e2b56a2f4930bcd2502fea88e57aa8892f83cec1b0b19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2233687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9511db534dcf19013c53826ea703a1c36b6a78e499df23501dff969181cd79`

```dockerfile
```

-	Layers:
	-	`sha256:a624d3366c1aa334ab7215e0aa77b3513585512f3e7d8700d6b92ce57fc2e868`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 2.2 MB (2224129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3ecff2c3b4dd86076b75dd0d8d33074c597f6d4fab8ce77e4aa840f0bc5589`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:872cbb9a2f2e915bdf75cccd98326ff82eac9896ef96588d18ba634df6660083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260253896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5521584fb8954bb83fd2c7033e1744e1499c601f07d4334cbd9b704a7c8eb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5376ff265040e57bb7e7d76f15e7dd7daa2f5fabd0a10ff689f6b2a7bc1685`  
		Last Modified: Wed, 19 Mar 2025 20:34:02 GMT  
		Size: 231.4 MB (231360298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ccd859d8df89f506977fbdb763f448683676677342d2046eef4cf54ae44a527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8c5f33a0e90e6e336748d3b595cda4ca30fe2ff98bc392e93466e2d96844b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa458612cd273b98e6e466b46d867a0c17aea542ac0b39efe1a54e45cd02417c`  
		Last Modified: Wed, 19 Mar 2025 20:33:57 GMT  
		Size: 2.2 MB (2226828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5950366204a7864f8bea5686a4353d066669a3d7e700ad2755b1cc7191506923`  
		Last Modified: Wed, 19 Mar 2025 20:33:57 GMT  
		Size: 9.7 KB (9686 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:df6565db4f03724d8e3c6160f0635014c880c1bc43f3a8d802e6698eccd0a7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266702269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b06298983a52f4b730d61f5050db059ca2c36499e5f39c2506c0af05cbdb9bc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dbd775d352df345f3ca29aa7e24e6a5ce65ba049960034829c32de5bbd698e`  
		Last Modified: Wed, 09 Apr 2025 06:34:33 GMT  
		Size: 232.4 MB (232361402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e62f2e0a1e246fbb538c4abbc75ef4288035628e7509b11158d8de64f3b339d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3668958c52c212acca9e0885ec059181bbd35d38020013ba13bbab8f1fefb2`

```dockerfile
```

-	Layers:
	-	`sha256:92682ca863b3d475ea4ab411876814d344177d95da1594a00692ba4ea094c987`  
		Last Modified: Wed, 09 Apr 2025 06:34:27 GMT  
		Size: 2.2 MB (2225453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24653b44dd8df1e6a87c021712dcc0578f37ff801698ab26308c23cab5fd553b`  
		Last Modified: Wed, 09 Apr 2025 06:34:27 GMT  
		Size: 9.6 KB (9614 bytes)  
		MIME: application/vnd.in-toto+json
