## `sapmachine:ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:077930e1e11588f9466356f5754e0ad1ad5cd3afcb24db043bd1b6cada0d3ffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:28336e18d53b839e4545e596de3ee24bd5e77e307a7ecf45ce01407b5fa63bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251800027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed051ffd900ff4c93ca429612cdd9b6e33c920003b220c4825cc6320d82f6cb`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d674a1b591c4d0c2e9dbe59224f41a31de1124bac807b8db0b6bbd41d0bfb`  
		Last Modified: Tue, 04 Feb 2025 04:48:47 GMT  
		Size: 222.3 MB (222264086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ba41802dc37e648078810e139a9e76f0a421942aeb4cddd1e57cce54b1a7c54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ea1a4b6dd661b9d8c2fd0a970e8929d3c37ce009ff6c1897a2aef07e5ea5d3`

```dockerfile
```

-	Layers:
	-	`sha256:338997e617d33ac4c7bcc643674f1765c53cf8181497ce61a6141072a67167f5`  
		Last Modified: Tue, 04 Feb 2025 04:48:42 GMT  
		Size: 2.5 MB (2496641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d53b84b96dd44b58127fe6ed47ae6d3316f13532645a1db3531d54cb0b8b3`  
		Last Modified: Tue, 04 Feb 2025 04:48:43 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6f2c35b398508bc8f989ff0f07a22a0d4b56eb25d751d66703f55b68c1c63442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247583178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c4dcc1eb93ace3d23cdabd3b3b19558ae2d87ac5aaaa6582ba82dea0cac41c`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec786f0041594d4177f326fae219aae0845cd69fa4e80fcaca8ab6c41407375`  
		Last Modified: Tue, 04 Feb 2025 15:21:41 GMT  
		Size: 220.2 MB (220224996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c89567b8b0b708538f2953c4829026d2df4d38234da4e9ac81a1d4f5f9dbf5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b599012a6c319a61dc24dc56d59ef4a1df741ef0bf1a896459211ab3b4ae47`

```dockerfile
```

-	Layers:
	-	`sha256:1814141066f4d5b420f6a8986fa8b6dd78cdba7c850af23a4ab6c11fc3fba1cf`  
		Last Modified: Tue, 04 Feb 2025 15:21:36 GMT  
		Size: 2.5 MB (2495789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc93146f9515b952b91f2fe48a003eb6d43ddabb9a109991a1c7d52bd82faed`  
		Last Modified: Tue, 04 Feb 2025 15:21:36 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5f736caccfc027efb9a7fcf3cdc396689ecfb92caf211b20d4c4b12efc43855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257741316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72101e16cbdeea7945a1b10231be8398572b114a41b3f6014c89cb1211dc6baf`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf4f4d425dc0f1fb7c359edd38b8b20680b2afac71ff0f934a3673a2abc620c`  
		Last Modified: Tue, 04 Feb 2025 14:27:30 GMT  
		Size: 223.3 MB (223293381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cc94df898df80929f70ae90424b413c15a0341a2fdd9180551e6a0c7ff89e424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54af12f5e61c8fa4ef7ec264c420b4df209f3d5fed3db88f6aec9a1a16354864`

```dockerfile
```

-	Layers:
	-	`sha256:a32a93f349a2b8ca1da105001b60a6d3d6e9ab91e82e13c4b0a6040a335d3189`  
		Last Modified: Tue, 04 Feb 2025 14:27:21 GMT  
		Size: 2.5 MB (2498106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798441a13a60d0a7cdc403bc5246c55fad7f9da8d2ccaa13a6bfdc1b4a7e9739`  
		Last Modified: Tue, 04 Feb 2025 14:27:20 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
