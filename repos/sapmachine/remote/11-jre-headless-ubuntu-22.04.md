## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:a38a11af38ffe36c171517beafae0d8672749f68dd64faad672c8a213a43df4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ddfa8bef4540a41ea284cafed8d86682eb90dca5b6a48829cd01ce2b495a94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78335659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e917e2ae9acbebff811a3bbe97894a48781244a7d7ae6dfecffbdc7446a10b9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee87c9a7c7d79df10a2b1749656239739cb55ee2c958235ec2254b29b62636`  
		Last Modified: Tue, 12 Aug 2025 18:06:07 GMT  
		Size: 48.8 MB (48798666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:376dd07f6fcc583e85aa7a1b51b478a241e238c9e10cccad85671a1be04ba0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ce132236ad3917560450e142ecf2d1e4ae708334e88ab4729af02bac027b75`

```dockerfile
```

-	Layers:
	-	`sha256:cf29789dd8dc26e70307e7ea3da14dfb509f37e02460db4307b34002eb7556a0`  
		Last Modified: Tue, 12 Aug 2025 21:04:46 GMT  
		Size: 2.3 MB (2299090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c311ddfbba2b7344f361dfd1c22ae37bb187fb1e9dfb6fbd5673f70003958d`  
		Last Modified: Tue, 12 Aug 2025 21:04:47 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
