## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:c0525e4595381715262f149e5cbad0d51faa2470c3182675c2493700a36e99ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0e935bb0acad990f8823e0cb0a37f764454aa8e5bc1bf0d51ca96787e12157f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83930023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34c8d08e56d4ea246ab14d5e738892dd14708c916fbff66264d5f4d11a395d6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96646e87b37cd7c280980cab7bc8f8e1c1b72f4222e6d583eb9af4cb689bcbce`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 54.2 MB (54212494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eac36ecea206f84e0a25f6a1fe45cb78164a103ae5e7ab7ccf9ba19722f40e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82454b433cb638304b57f8ad455983b8f4b2a0196fc45cf8ae5b38a120079f3`

```dockerfile
```

-	Layers:
	-	`sha256:2d02e6f50e27a596702f9675d05866cfdcd770166cb0a8ee16f0ccfc31ee7b66`  
		Last Modified: Mon, 05 May 2025 16:37:03 GMT  
		Size: 2.4 MB (2385584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bab5fc2a72acb617c962d502b522f4ccc1f8ba4856d09764738a7c0c9bf7d91`  
		Last Modified: Mon, 05 May 2025 16:37:02 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8ff54bb87634fd1dc2869c25aa819c86ec7b75fb56618b52505569cf63c204c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82511859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e4e74c0c2df8600045c48f341e6eaea1c3ac02825203f992a32628dee2a6d4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa880cf08ae92e6b514b318c9de940bb5b48a6ce85ac06bf094a988616350d96`  
		Last Modified: Wed, 16 Apr 2025 16:38:22 GMT  
		Size: 53.7 MB (53664901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d87ff65550803ab7e8da51649944b23aae31a2b06c70b8812ef97fb5300b7af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82562c44d59cf021c1ec7ef1713f3c812f921de9f128f04064c081ab4b228c`

```dockerfile
```

-	Layers:
	-	`sha256:28ba48849745e97917660419f2dd7b773ee7777edfe9dfd29fead6dac51048a5`  
		Last Modified: Wed, 16 Apr 2025 16:38:21 GMT  
		Size: 2.4 MB (2386072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7967fe8f85bb84accaf264680a0d426663b7b6429f593b566370b30e9d1baa69`  
		Last Modified: Wed, 16 Apr 2025 16:38:21 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3552a8a9a316b675f69f25fdbaac86a6caa4e367c401668a201fa9af079faa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90182510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab6e9c89f6574e6a105c6ee2c981acf96560a8f37772873e9134b6f3abca8c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9272eed01f3b61a266e1a186241e59c73eb08982477f55c90c537d7b6fa640`  
		Last Modified: Wed, 16 Apr 2025 17:06:37 GMT  
		Size: 55.8 MB (55841643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0309426a90fb6bdff5e0c287e9305fb2c640d7f61a1da9ac6f323d5915ec14b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a532e292a8fa30ceb9c6e24474a988fa8d3a96b95b30460437b4707c58740ef`

```dockerfile
```

-	Layers:
	-	`sha256:42fa8f5a9bc32d3ae7a2962368bfd0e08643c34e44cbe6600526e2d8bd62ef15`  
		Last Modified: Wed, 16 Apr 2025 17:06:35 GMT  
		Size: 2.4 MB (2389531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6dcdc801614f70f06d6bcfbbe1dc75cb801ea9c378b46077bf9266d6f5722bc`  
		Last Modified: Wed, 16 Apr 2025 17:06:34 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
