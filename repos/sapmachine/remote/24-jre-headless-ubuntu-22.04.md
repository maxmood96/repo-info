## `sapmachine:24-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ba6132659ea78fc3b1e5434966ce8426923f056403e879579c28253bc0d464f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d15dc91bffa57c75461a34b04a4773ba3cfa5c2ab2ff897a49144b541db23ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95987929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d54552de83913705aaf65987837e63ad952cdcb5886cf2aed67c574213dc64`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64f8c171267e8e290e43ef1fe897cdb3d3de42ef403db0c150e2877f2d3623e`  
		Last Modified: Wed, 19 Mar 2025 20:33:21 GMT  
		Size: 66.5 MB (66451988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d0a16dcb85600561cfca9d7b6bb6b23a9b627abbc1205a1f86bfa0b4d19f9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b59bd832e3f8b7eed09e2c5bc5325a5cabe9d39eea0585cfdf1d9a3e9ef800`

```dockerfile
```

-	Layers:
	-	`sha256:1b36dd234755a25049681c80034e12b6a3845ba264f58a4f2f71b8ff6de86819`  
		Last Modified: Wed, 19 Mar 2025 20:33:19 GMT  
		Size: 2.2 MB (2173146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5a54835e5d518a8aa9d2d97cdcf56a3d44775d37560c00e0269ab5b57e2567`  
		Last Modified: Wed, 19 Mar 2025 20:33:19 GMT  
		Size: 8.9 KB (8887 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ec4db1e57b8743f133d7e90b3c336fdccb8617c80e0b193ad919aa72c2c79333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92799288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d896ff1d4b62324bace2e7a8827d7b7415c50066954dec93a406311ec052a37`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c5ff60b17046c425158d10409d1743846f3bd1528dd7698818474942ca06ec`  
		Last Modified: Wed, 19 Mar 2025 20:39:18 GMT  
		Size: 65.4 MB (65441106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3165dee0356f44c5a0b0981aaf898e04571c38069cc717358b757b08cc920bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d7492ca105cef29feddc7283fc5ce5cd4130df2b6c39e4f0b5178c10742565`

```dockerfile
```

-	Layers:
	-	`sha256:757c6173abf4767c4f8cb84d3b7d6ff3b7255c6c9c18ac1b2236edabe0dbb033`  
		Last Modified: Wed, 19 Mar 2025 20:39:16 GMT  
		Size: 2.2 MB (2172815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f142239bc18bee4b57b5cc38ab5ff2e2418b9acf6d06b269f989a668135410c`  
		Last Modified: Wed, 19 Mar 2025 20:39:16 GMT  
		Size: 9.0 KB (8991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:632494391c9a80de9457fed6b920ebbc0c2e2bd86f144fb31fd8baa29cc2a94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101985225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb9a29963e44bc585aa5a0ae7719e26cde44a18452ec30c5373323826c84998`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17cd6a2b835b894bcc9cfa75eed20c3527271a82d53fcc3e8fca932765dcc7`  
		Last Modified: Wed, 19 Mar 2025 20:43:37 GMT  
		Size: 67.5 MB (67537290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bd5f7c28dafac6eb32114ce0cd65180898a19e09af781714baf350595868c840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993750f3a6e88c47b479fcfb994e2b2d55fd8264147198d73ccb6a3bffe0679a`

```dockerfile
```

-	Layers:
	-	`sha256:7baabc867fe165ed5df391fda3735b84cd28d9db4a1cecf79f9bd891b489e492`  
		Last Modified: Wed, 19 Mar 2025 20:43:34 GMT  
		Size: 2.2 MB (2176427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7bb5b049f86bfc456891c0acc53bf48e86b215d930fba1a705450bdeb6c3c7`  
		Last Modified: Wed, 19 Mar 2025 20:43:33 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
