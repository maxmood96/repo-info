## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:78fa72d6afb71fb81c83e780cdc7038a8cff8554f435ca1ab070db501762b10d
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
$ docker pull sapmachine@sha256:785f540e103824d22eada2d5591ac939610f6fc6225fdbb5df33cec6ce081e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89926875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f2f21bff0a4eb61172dacff8b93c36309933233c5a82b6b4f3bdbcd0c1b10`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e908fe244f58aeb936911523cd9b98d0b70f5cd2d79bcc79f12177271ef362`  
		Last Modified: Tue, 02 Sep 2025 00:18:42 GMT  
		Size: 60.2 MB (60203811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec8f254ae42fced5dd224e7188797cc111d186a9039c01f49e4820c7ad922818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af7fde26e1b32d38320ba96f93f4eeb9606a1b7f34d52ca64ef3597d14d076a`

```dockerfile
```

-	Layers:
	-	`sha256:08816e97c7ead553ed52e413ad151deb51569b1085d179a6e8acdbc5bd85ee54`  
		Last Modified: Tue, 02 Sep 2025 03:07:41 GMT  
		Size: 2.5 MB (2519618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3126ec16a36c3baa95acb2a9f1f92b97a1779426dcdba69d1a3ff9a21de24fc`  
		Last Modified: Tue, 02 Sep 2025 03:07:42 GMT  
		Size: 11.1 KB (11070 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b21546eef0171561baa970c2283b3fe462e610ae978530fc919eb0800aa698bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88245434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7968273759e94d8b4fee738e9926f3da0d88733c18e835dac0ae6bf5b3229d82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1293005399ce0bb7b8cf1e5d7ccc3482b668b2e1cfcc0b27a26b4409d2bb8d2e`  
		Last Modified: Tue, 02 Sep 2025 03:07:54 GMT  
		Size: 59.4 MB (59385194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05003784e840c2f7f05a8bbfcb9a2fe3123215dbfb5fdef1199ea2c4ca2ebec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d3901f5bff89f7847f8c65a3080d3d3fba9c40c3942a57ec3ed6fbe0fc4f58`

```dockerfile
```

-	Layers:
	-	`sha256:94c04d59d1cdb2cf77d7aa9aac906249d61ec9b385d85c551f625e83109e1bd7`  
		Last Modified: Tue, 02 Sep 2025 06:06:59 GMT  
		Size: 2.5 MB (2520170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d9badba6b78dc0cd888eb799a9d4353bebac9a84c989131e775abd25d5d9cc`  
		Last Modified: Tue, 02 Sep 2025 06:06:59 GMT  
		Size: 11.3 KB (11258 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:faf5140c72f3ccfe492557d9635585911f648440148a1defff132a523d01e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95765697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d5e7056b8e38e93cd02a6fc83870a49ad85520a6e9a874bc464861b53b3a63`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b78ae4eb2380cbb956456b2fcb96f5830621a15160d5dd226c664a502eef51`  
		Last Modified: Tue, 02 Sep 2025 02:04:58 GMT  
		Size: 61.4 MB (61436164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:300f1b642cd8797b30e4c3500e84359f28aa38f014dbb6ea452630e6e21623ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6b4fed1d483454fcca1b7f130151b30df2e6735befdfdb473b3a6f2fa126e0`

```dockerfile
```

-	Layers:
	-	`sha256:f59060ff1d0cf44375e757b62f35665c60ae0e4d627bbcb0adde345d9ee20ecb`  
		Last Modified: Tue, 02 Sep 2025 03:07:49 GMT  
		Size: 2.5 MB (2517717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a2762bd91b3ef3688d3b9cb3e82e3609a94804789590aedd5afed4e5235a25a`  
		Last Modified: Tue, 02 Sep 2025 03:07:50 GMT  
		Size: 11.2 KB (11154 bytes)  
		MIME: application/vnd.in-toto+json
