## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:6af495c68616c135908a63b4fcab017047c6d0b0f1a38192acca33914b6996fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ffd84fd47eb6fd561be90cfa2313cf975c7f7b3792f1481a81da7dfd557e8bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78335625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966cf242b7ecfac1a7f5c96439e46d7d36139fd4224731427ab63b8e902ac38a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:39 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:39 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446cd33b2d776ed12b2c9a34a483f34d3fadecf975c7f5e17eeb2944dfc60bbb`  
		Last Modified: Wed, 17 Sep 2025 20:14:51 GMT  
		Size: 48.8 MB (48798690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01fcca73a260b67556f29a2cf2556a1626367fa14478a22c62c1d05ae6f4c10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bd8bf16d30bba6eb7a829fd2301d6ff0d868007b23812d6bbb818e0fd6c6b2`

```dockerfile
```

-	Layers:
	-	`sha256:837a8f2c43299213213e25ec57d8e155acc68a1fda7fca7ac57c397cde54c767`  
		Last Modified: Wed, 17 Sep 2025 21:04:30 GMT  
		Size: 2.3 MB (2299106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db15ca2afc8c130fe1ee9fe1fed018e9ca0f4524d23b572a1261b5e7f06ed4e6`  
		Last Modified: Wed, 17 Sep 2025 21:04:31 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json
