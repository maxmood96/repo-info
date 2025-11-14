## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f11fe5ecd7c169edc6ab47a1364fc56506238bafcbdfc1f49c97430aa4af3b98
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
$ docker pull sapmachine@sha256:c083aebfcc23afb6319f964f007e31934a7865af7c22f36aa6b33502063d8529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94391213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6867cb150025111a96056019bbb417be0eb16d36914d254be9cfc243308c1635`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:31:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:31:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:31:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a642dc6462bf6dd5235c125f928efe87a780e347f91750bd3eef337ef7c2b08f`  
		Last Modified: Fri, 14 Nov 2025 01:32:46 GMT  
		Size: 60.1 MB (60086789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f9258e69d0402e54fce4dc0849fd25132acffd708c31a2f93642025608ec2897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90448734f185a0f39dcc704b2a77b70932f2e827e507af7c72e99b6073ec148`

```dockerfile
```

-	Layers:
	-	`sha256:7e0800fabb2efec0e9749393e2109bd06f9e4cb7e23fe55faee81a8b6da0bb01`  
		Last Modified: Fri, 14 Nov 2025 04:08:11 GMT  
		Size: 2.3 MB (2270810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075aa1803b90542003917226fafe0e32099a2b2ac7cc09e6149f4773bead1ee0`  
		Last Modified: Fri, 14 Nov 2025 04:08:11 GMT  
		Size: 10.3 KB (10288 bytes)  
		MIME: application/vnd.in-toto+json
