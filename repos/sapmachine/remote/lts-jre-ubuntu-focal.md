## `sapmachine:lts-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:c419e2bf93df611e82b4988c10f5349b91cf00f627ead7bee8762ba754bcf040
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:bb6dc4603d76b68b2e6004dbb0aa0cecea5f4652f3a4a5b1f7b4baf2843edd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86777534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e063249f93f833a4b5e8d1e94a59a9e35519c25bb5821dff1694a7cde1597e2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a397c099f24646eba5908019661fc006de4997b03d5771d51b01ea93c6d85`  
		Last Modified: Tue, 28 Jan 2025 01:30:17 GMT  
		Size: 59.3 MB (59266474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1257a03e3cac8c9e4e770c86ff409bd04d1f19ffb4e61a9d84230fb12cf427f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965d60079ee7e011215b4152ba87b06282306d31179b6763fa17dca96d7162c4`

```dockerfile
```

-	Layers:
	-	`sha256:9748677630833a6b7fff1edf6b4fca386f1e311d9c842f75f7bd98fea062b15d`  
		Last Modified: Tue, 28 Jan 2025 01:30:15 GMT  
		Size: 2.3 MB (2301121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a939059db611806a82d56727f6e74a848274a59c7168002dcaecd1accceb6a90`  
		Last Modified: Tue, 28 Jan 2025 01:30:15 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:86a373aeaf46931ffc4f91e51ac27d2c1ca2f8e7391e6b23aefecf4188900e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84418137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ce618332710fbaa19b39a47d2bea992e89f5bf8a7be40d6db254a3673ae8db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08996497c274dea7fc4e853341821af1a98b169d5b984a8249f532162d3544`  
		Last Modified: Tue, 28 Jan 2025 02:46:35 GMT  
		Size: 58.4 MB (58444309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90af6417200a7c46d6349add821146384fe36a4be37837e4709f81b3bed054f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003e8367ec523d0e8a5c9b2cf31b676304e1240ea2f21bef693c0bbd55cd4f89`

```dockerfile
```

-	Layers:
	-	`sha256:089225c48cff6b8ce1536755e44c77c7b4deae0b7e94125f610aa66397dd8e11`  
		Last Modified: Tue, 28 Jan 2025 02:46:33 GMT  
		Size: 2.3 MB (2300783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df18c3c7a4287e082290c5807d408706f13477c4ae68fa6fb8855612ce1c3f2b`  
		Last Modified: Tue, 28 Jan 2025 02:46:33 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c744236b6e72cbe6b22f4886cd27af89895c9a6df41feeff5365d974d41aac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92544135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebc37e1cb328845ce47cb79b141868f072e583faf3bc28cf2b6ede36d0bd36`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4f8eb21766997318bfde5dad610db0d9f6702fee17f2225367f72baf1c7c7e`  
		Last Modified: Tue, 28 Jan 2025 06:04:46 GMT  
		Size: 60.5 MB (60467629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c50f7f27654cf1f7190126e1d183167bfbac8225eaf95a5fba9e713f2264aeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed4b3eca01bf10aafca557f64154f6b5a7e742f5b4cbff4e1bce1e901f5b5b8`

```dockerfile
```

-	Layers:
	-	`sha256:2012f190821dac4f7772f0622aa4a2ed76ba48429cdf94ab15c4a00c80902fda`  
		Last Modified: Tue, 28 Jan 2025 06:04:44 GMT  
		Size: 2.3 MB (2304900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ebd5796675487e93f767d9da6a9d4cb3898006ab58e32f519a221ca7922666`  
		Last Modified: Tue, 28 Jan 2025 06:04:44 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json
