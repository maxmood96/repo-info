## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:48634b6cbd3de1cce2852a5e5bc1299c2e5ab2b420d8611ae28499e530615d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5a1a294e1acf09fbcac3c2f09fbb0783548d31e0429104cb494b714f2e93552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78315703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8bfbf13f3b673b2c5c548450140bc8f06b7bb923ce75e5e9b2a579d892c1a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a0d0b0819bfc66991064ef61abb02fd5bc930433370556dd056089e98bec18`  
		Last Modified: Wed, 16 Apr 2025 16:14:16 GMT  
		Size: 48.8 MB (48783338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8a1a3ebc7506d44c47b04b02acff2082c35c79f059e637febe9403eb0cf0a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cac68b9f5a42aaafcc2c5c1b8925fc601e26a936eb7f0052db35ad132a8778`

```dockerfile
```

-	Layers:
	-	`sha256:9393aca8f70928718db2f478e049a81797424517cb4177fb059e7ac545bc0ccb`  
		Last Modified: Wed, 16 Apr 2025 16:14:15 GMT  
		Size: 2.2 MB (2170998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ae39b3a3673cced0ddf50a9732ad3e09f7d74ca42b1d278900c50472a8f929`  
		Last Modified: Wed, 16 Apr 2025 16:14:15 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
