## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:a5dabf3995dd6b30255bf21d79d2e7cc687e0ce1f07115edb3c44ca602945c70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:22e9d7b4564fbfee39650648864fd19f378ca44732d87eb83a4cdf7bdfe07192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83927611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbd130ae58e29a5efc87df72c66897eb7a9c093a748e94a7924efd561833581`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356e17c31040d3ec73327337e2fa2d19c46ea22b9bb49802c6ab525773ecefc1`  
		Last Modified: Wed, 02 Jul 2025 06:07:35 GMT  
		Size: 54.2 MB (54209245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca91bbc89b60e7fadd4a9baa2eb473590959271e5632b34ba6e6444e9bb8ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7e21cee1669697c82a7550da7d54aff9ebedaad49b870838c025362fcced36`

```dockerfile
```

-	Layers:
	-	`sha256:9e4348dbe7a2abdff48e7c02fdd5f609e1e94ff645eda2ae31c77ed7a1b6bb08`  
		Last Modified: Wed, 02 Jul 2025 06:06:12 GMT  
		Size: 2.5 MB (2516750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3682c7357c26b33209a6b4b713432124297eb90321b6184eca22f7681d0af100`  
		Last Modified: Wed, 02 Jul 2025 06:06:13 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:aa0d5d3a9062e80ae7cd3b26421ff5e9008992681770a746c366d7d677e294bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82517325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021dbf6da4c2bafd3a81207b3281151a31cba9977c8ed0db1314f23de2893a21`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324c412ba16aea76c61e952fa9e273d676f1af54ae97bfa6c7602888a0f4c8d`  
		Last Modified: Sun, 08 Jun 2025 06:42:37 GMT  
		Size: 53.7 MB (53665426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ad5b11faf6073d24d47c9b705fd77b02824465dd9eec6b098b9599e008d0121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cde9e3b67bc56ebf8cd171542769a446f4eb03b3d366dfd4bf5bea665479010`

```dockerfile
```

-	Layers:
	-	`sha256:fae5e7f852b06f89c5b7cdb3ebdfc4beabc12f7c59d172b1a10807da3930fea2`  
		Last Modified: Wed, 02 Jul 2025 06:06:17 GMT  
		Size: 2.4 MB (2410284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a68b7eb95e946b092104ca0669c55854d4b11c5878836654d064de255d60d55`  
		Last Modified: Wed, 02 Jul 2025 06:06:18 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:18d8908d3bd223e83f702ff065c1f498dcf14d45526b4edc7b69fe6799939e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90151606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca1742f13d472de190c6b9fdce760eda4f144fbf9a5498177982d8ddb9a96e8`
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
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15182c7307477d79c87388911d2e1163a9f053e449ba45ebbc6ba91df72d107d`  
		Last Modified: Wed, 02 Jul 2025 05:01:05 GMT  
		Size: 55.8 MB (55830100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:702a61f82447479344ed1a90d6b5b58755e9fd117c57d45a71d39b14e31d1bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c11621db629c0acd9194c4d728ec54fbd287216dcaa9fd2ba7fbcd416e2cb4`

```dockerfile
```

-	Layers:
	-	`sha256:dbb1336cd175aeeab647d147e2c39048038e61466ce4540f5e3534673ff56239`  
		Last Modified: Wed, 02 Jul 2025 06:06:22 GMT  
		Size: 2.5 MB (2520835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89c3d222dc996e0fa50c4276594a47210e36edb46843a6d868da8aac6dee700`  
		Last Modified: Wed, 02 Jul 2025 06:06:23 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
