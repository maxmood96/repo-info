## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:e466df5d4fb15083cdcf50d45ef926ddfbfaca2d346a7410e0fe43a8d1f921ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:dbc453aed09472a89f877cea1d133d21d5fb1b89e169100b253f45ceac2b3ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80118639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e40a3de4576d16dc22f2c8a61a7bf3190c7bbaf5658788255bddaada11af437`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a2a16f1e2bc91332edd511019a41be31a97120619344737dfc5098c3e39042`  
		Last Modified: Wed, 13 Aug 2025 21:25:46 GMT  
		Size: 50.4 MB (50395424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bd42facb7cc237b2c17b61e40051323b7c2be71eb18d1dbd21f549f6024146db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6e059920f9fec733ae015d66cc125f61f61b34002ea005eb97c52997e10b2d`

```dockerfile
```

-	Layers:
	-	`sha256:8ebb2967edfc0b55b360cc07bf470aa80dc7ddafc28e9b42fd0b31e75d036dad`  
		Last Modified: Tue, 12 Aug 2025 21:04:37 GMT  
		Size: 2.5 MB (2523629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91da294bbc7620e66076d83f442767a84974460498128d6eaacd25dedda3fac4`  
		Last Modified: Tue, 12 Aug 2025 21:04:38 GMT  
		Size: 10.1 KB (10093 bytes)  
		MIME: application/vnd.in-toto+json
