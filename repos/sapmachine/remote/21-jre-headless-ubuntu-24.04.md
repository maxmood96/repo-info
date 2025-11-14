## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e552d045d16db764d1d668b407289ca9ff630eb1bf2d555457010fbe05fb7291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:91a5af7603ac2aeee92b4278a9256f0e37865d4f9970fb5e333b9f90416e8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88770184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b7623602aff34748ebd27970c17fc4b095076a65a3fcad0bfecfc97700071`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8e36397ba4551bc9ca99838b5c49c357b7fb008047007e10699ecb6f4c2426`  
		Last Modified: Thu, 13 Nov 2025 23:38:38 GMT  
		Size: 59.0 MB (59045496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76f7ffb6153440616ea8af9c0b6e341bcfb58d9e563114f9716ef4f5f66d9e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4881c09829edf6cc5dd2e4e88c8a7c796dbf135778e679e06e9db97ba1ae34e`

```dockerfile
```

-	Layers:
	-	`sha256:aeca269c81cf228e84ef291ab85f00ab39acb3c37ecafb6b42c9948254806afd`  
		Last Modified: Fri, 14 Nov 2025 01:10:24 GMT  
		Size: 2.3 MB (2272810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bec7b0c1e442c55bfbc37ae0f640fcacce58e83213a799fb68c2dc2c0ac8dc1`  
		Last Modified: Fri, 14 Nov 2025 01:10:25 GMT  
		Size: 10.2 KB (10219 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:38d1e28f3134c7ee7ab8e79d62689efb973f0cf5828705171b50137fc9e5a2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87088198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff07a76f7d12abad11450969ffc8297ee4ed788c18aae899709dc7a38f670d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:37:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72677bdb2d5d46818624acc162a4a414af5589fd49f39576461e2d235fc7f057`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 58.2 MB (58226241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6262d5c197f072c1b1a085b45dd2c72b075a57b20aed42768cf7e373ec4a90a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2638568d1145083739ecdc8625c5e53c74856b30751e3f2fce7a844f973ca1f4`

```dockerfile
```

-	Layers:
	-	`sha256:9aa396796a94d5dce41c927aa87214173a207c1143445806c9119f86bb3b9c56`  
		Last Modified: Fri, 14 Nov 2025 01:10:29 GMT  
		Size: 2.3 MB (2273317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11389c22976e0a380d1d40079ad6ced06f10e43696200c7fb7360112f1480891`  
		Last Modified: Fri, 14 Nov 2025 01:10:30 GMT  
		Size: 10.4 KB (10370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:423611c56fceba0deae0d38eb34ec419f959c2c06f08bf44d9523a50507edd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94390374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743ffc13debad7bfac3272ff6589e581a494049362249d5d6a0f787fdd1e5cf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e7c13c586c2b237847a486d86be2132011c4cba7c3309595b3d2dadb4d329`  
		Last Modified: Wed, 22 Oct 2025 11:53:01 GMT  
		Size: 60.1 MB (60086849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:782943914ea5a5875980a4b1c914bf45cb625168a95c5c375a0cf8813c28b308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975971d40a8f909834e79b5706ab3219ac543ccd10ad9b8455f9a2578afd4325`

```dockerfile
```

-	Layers:
	-	`sha256:a71e14bfe05d14036df8cd2ca48b19471b3e4f7a9e7a1365fae916e69f1fa102`  
		Last Modified: Wed, 22 Oct 2025 15:08:07 GMT  
		Size: 2.3 MB (2270810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260e30fc49d6e44ab5bde173ef2dbea6ae532e361fe03ad0d92b65aa6cabe6af`  
		Last Modified: Wed, 22 Oct 2025 15:08:08 GMT  
		Size: 10.3 KB (10331 bytes)  
		MIME: application/vnd.in-toto+json
