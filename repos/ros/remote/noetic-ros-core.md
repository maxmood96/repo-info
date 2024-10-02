## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:cb53dd5fc4b945940f4de37fd48f14b9d6cbef11d27cc5ab1dfc1e51b59edc13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0d07af5e45d229a70f1ba4db6d225d98d45897ce46c8151f9bf80730615cc0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211100130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b926f81d02c44d3895c92b7348b7a905796be12e3001426486b8045d1c235`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce9cbddae4588e8fc7fbd8a300da9a758a948cd04ec3b1368624a184de13e71`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 1.2 MB (1198681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83ce5ea8c74b3a8fcc0da7e664a139640a83469a255feedac928b11410dee6c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 5.4 MB (5361806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10601306d61ee865bd7a1828296a8cea1d16886115c83b655becfee0c1eb596c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1783bc90edda4ccf720a22d16ac2d0d51ddd52f7adfb85b8e78f8b55df2b12c7`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53631aa1770cb44838f8b3c2ec05c4fa0d7f3448b7902d982a8c4bdbc99a32d8`  
		Last Modified: Wed, 02 Oct 2024 01:59:39 GMT  
		Size: 177.0 MB (177026126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ca5c651827208ff792ccdfe8392da87f425c6a0a51a8da7674ad1f0b38f45`  
		Last Modified: Wed, 02 Oct 2024 01:59:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:31f1e235960e93a826517a1eddf7c912a79ec573a1d9c73c4bf18514ccc320a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26126951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e79bc251e97251864690b8363ad9826aa8c15332a5b42e45aae2d7c5a8342e`

```dockerfile
```

-	Layers:
	-	`sha256:388523c274721af1294fb4341df4a18ff416642a44637b098b762eb946ad9cd4`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 26.1 MB (26110823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae703e962e4de5bd8f0222335dff87dd2e517fa33bf027f27e6614104bdb0d2`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:0cbfd2f06bed6bc18ebdf04c7712e49489bfe61def7f150898e8cb587a3fb511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186821005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393c0c83f56de9e250897a7ed19770b8b711cacbfc40f656c0c7de6bec2f1abb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:11eda96b18d1f3db85ac2aa91b88e0f8afbb12b21c50d6dfa06eec4ced4c76dd`  
		Last Modified: Wed, 18 Sep 2024 05:32:52 GMT  
		Size: 23.6 MB (23619920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e426c7b7c694def02912292361e2695558e37ff1afb19f3d251479df029f8`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 1.2 MB (1198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdf3697de627e9d1ed3bb19927623ab4c49cfa682d7fc8a960832f73a7042f3`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 4.5 MB (4487307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3128b56544232e4c8e974d146e599be7050e87e5c52da65e4e5d4cdc804fdc77`  
		Last Modified: Wed, 02 Oct 2024 03:51:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ade4de2e774de5ff58e31a47d1c5a493c2793085116b0368893652d49289b`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0595a66a5286ca6f2c09ddc1480ec9384b51bf3f0a036ee5c7a35fde1ded9159`  
		Last Modified: Wed, 02 Oct 2024 03:51:43 GMT  
		Size: 157.5 MB (157512590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114f75e546f007a1cdf08d0e0edbdec7643a3992321e83099513616133e099be`  
		Last Modified: Wed, 02 Oct 2024 03:51:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a5b78b6fec16fcc421e26446055d1f9cf74335800da809c51a376eae102afe4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26040585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782cdb7d58f92a59b8502d66c3524a7d753d964c11dd1cf87e6ef21d7b177c9f`

```dockerfile
```

-	Layers:
	-	`sha256:c11e870523c7490325048e95935cf075e22f5195b6ad9223b6bdbb6b65cadc87`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 26.0 MB (26024351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8b7058b7c181e0cc39bcc01469b046df4ddc3b7432237d722950569d2fc1b`  
		Last Modified: Wed, 02 Oct 2024 03:51:38 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:535af6fbc8f7d627e12f1873f5928d1f0b865c99f7af36e04f125b07cb85c373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203950967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165911ebc4653a90248fc55e1cad3dfb8ed1b3e54c0069170a8b991739ace59f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d4290e116e35eae1f83e61d030b4d088b95b5e2c40ed078fd3b265261708d`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 1.2 MB (1198664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88877cfa8c13065d2ddb4860be1c17a12c0e4ae2c2ea0763231890ddeacf55`  
		Last Modified: Wed, 02 Oct 2024 03:36:30 GMT  
		Size: 5.3 MB (5342081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab5feed6ccbfeaaaa78d06ba63d061065b8770efc6f2bb286ffb307d46ee61`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220127cb75259289f6f01775c6e6edcf220b331062be4654dd6516eefd4df547`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe60eae5591c9e6979d96562bdee2e70645f096510a26fe57899e826966b977`  
		Last Modified: Wed, 02 Oct 2024 03:36:37 GMT  
		Size: 171.4 MB (171434164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33047cc09a47eca1deaeb10981a2b592f2f8bdcf137e3dda26a45aa9001b787`  
		Last Modified: Wed, 02 Oct 2024 03:36:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8e780e059ccf69c34ad4907a22238f85810d855d09ec905e8608e6c65af0e56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26049161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42967fc9bd60145e78df579cf142257dd7369632a68ea2f71e2a56ce4ba51e45`

```dockerfile
```

-	Layers:
	-	`sha256:cddc335acc692ad665b395471757cc34a287cb226a6340cdc28684be58cd3d9d`  
		Last Modified: Wed, 02 Oct 2024 03:36:32 GMT  
		Size: 26.0 MB (26032899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5bb0ec82a722bc655815c0f73ca611fd15bf75f788ff3abcd572b36de98583`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 16.3 KB (16262 bytes)  
		MIME: application/vnd.in-toto+json
