## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:18f7b5f29b9ab9db3c343dd90156edb7d44c4b8fa65965da823e232278916acf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:eaef6147d2d22a91b9f00581f020918692f8c4887a3077c1af533cb9c679bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89473762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaa5aaeafe9a9733ab44d587899ad52d936011a492e49d95cefee92cf697a7e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e818870235d4fdc19ef88b66823f495e340951d8c1971c4d6820179bd7fd9`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 59.9 MB (59939707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7daea58bcfec36d64cab4ae8931383c5fbccf06acdff0941b545284164a3b1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e081a8f6d988fecb9d893ac4c508716a96af86349fff61a4ee460b381960de`

```dockerfile
```

-	Layers:
	-	`sha256:43c1fe298a45273090e7f68a39ea7e5fb000227e4704d2649c8a7cb4d2b17eea`  
		Last Modified: Fri, 19 Jul 2024 18:00:19 GMT  
		Size: 2.4 MB (2389425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be24238fbb6776a7a0694fded9f07af00eed2a4f90747ffbb68db6becbb38a82`  
		Last Modified: Fri, 19 Jul 2024 18:00:19 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c1494684e2318c2745d753fc629746fbe89cf1caac18cea2a25afb4b569b8e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86357273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c53a8d4ead31e12cfbc9f5828088ff02cb70032f32c60a50cebaf6c05257a4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64121ff37ad2cc2878c72421f84d6850a563684a492b8ae4b98be8ada6047670`  
		Last Modified: Sat, 20 Jul 2024 00:15:15 GMT  
		Size: 59.0 MB (58997248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f44f19371f6a2f9095154d232dbff470c0d2986df22eacc77f37ee8862547ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f751e552ce968fc55802b08c30497f4ca5f1ddb5f00b5363e53993f60557bce5`

```dockerfile
```

-	Layers:
	-	`sha256:5a82e405766974fee4d7592e10ca5ac2e36200ea71445187951c11e8f3b53743`  
		Last Modified: Sat, 20 Jul 2024 00:15:13 GMT  
		Size: 2.4 MB (2389129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93c3c7c90c83379ed2287bb7ad8431780076e7eef9cdf1618e0e10a671c60e`  
		Last Modified: Sat, 20 Jul 2024 00:15:13 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7b0e83769e20956e02fb7e81cfec8001d8a417230cab1df865abb49bc38494a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95964270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc9500a86cf2dcf008ca92bd87bcd87553e1739a7e81d103ecbaf4043fb1cb9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dde2ab4cbedb157f79d4119ead445c8cd2e9b1905d9d26344434e853fb6e661`  
		Last Modified: Fri, 19 Jul 2024 23:21:17 GMT  
		Size: 61.5 MB (61503189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbeb182e43ae145c29c609bf49ab46de3290e727a815aded4ed6eaf14ae5c15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d378a9b130e7f4ea761948418612da12c509944ae86d7256ae9055e03f8516`

```dockerfile
```

-	Layers:
	-	`sha256:2c7d208ffd913e8ddc2120c07f984743f134ed1db39f39d96d1c18615091f474`  
		Last Modified: Fri, 19 Jul 2024 23:21:15 GMT  
		Size: 2.4 MB (2393416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2369ce3fb6318c2c2a78f89d928333281b2f76fa4650699cc1b6c53e571c7a`  
		Last Modified: Fri, 19 Jul 2024 23:21:15 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json
