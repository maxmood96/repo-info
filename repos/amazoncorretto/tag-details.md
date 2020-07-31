<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.8`](#amazoncorretto1108)
-	[`amazoncorretto:11.0.8-al2`](#amazoncorretto1108-al2)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:11-al2-jdk`](#amazoncorretto11-al2-jdk)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8-al2-jdk`](#amazoncorretto8-al2-jdk)
-	[`amazoncorretto:8u265`](#amazoncorretto8u265)
-	[`amazoncorretto:8u265-al2`](#amazoncorretto8u265-al2)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:3cfef9f3e00105236a1ecbaa33a79e7ae89daca3f66113f0a4da3ab8de05f9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ffa3b357b53c9cf989731c121f41f7e1f51b0c496c8e1e00fb006e45060a2c2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206838882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835432d05b3b11d4ad1fa33bbf3cec5cb0c35726b52123db4baa51aaa0c8cd11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:20:25 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 23:20:49 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:49 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b279024f090539c4f61036e7224048b5d4807bd884699f33112c444a2c619a`  
		Last Modified: Wed, 15 Jul 2020 23:21:33 GMT  
		Size: 145.2 MB (145154200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2c27ede8c07f9fd65f3737a6548d7d0936fb6809e155ac3e2694affcb5df619
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1c7e505088322f662ceda52329d7ba40d18d0f1ee0116f64fd3309cbbbfd09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.8`

```console
$ docker pull amazoncorretto@sha256:3cfef9f3e00105236a1ecbaa33a79e7ae89daca3f66113f0a4da3ab8de05f9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ffa3b357b53c9cf989731c121f41f7e1f51b0c496c8e1e00fb006e45060a2c2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206838882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835432d05b3b11d4ad1fa33bbf3cec5cb0c35726b52123db4baa51aaa0c8cd11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:20:25 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 23:20:49 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:49 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b279024f090539c4f61036e7224048b5d4807bd884699f33112c444a2c619a`  
		Last Modified: Wed, 15 Jul 2020 23:21:33 GMT  
		Size: 145.2 MB (145154200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2c27ede8c07f9fd65f3737a6548d7d0936fb6809e155ac3e2694affcb5df619
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1c7e505088322f662ceda52329d7ba40d18d0f1ee0116f64fd3309cbbbfd09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.8-al2`

```console
$ docker pull amazoncorretto@sha256:3cfef9f3e00105236a1ecbaa33a79e7ae89daca3f66113f0a4da3ab8de05f9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.8-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ffa3b357b53c9cf989731c121f41f7e1f51b0c496c8e1e00fb006e45060a2c2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206838882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835432d05b3b11d4ad1fa33bbf3cec5cb0c35726b52123db4baa51aaa0c8cd11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:20:25 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 23:20:49 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:49 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b279024f090539c4f61036e7224048b5d4807bd884699f33112c444a2c619a`  
		Last Modified: Wed, 15 Jul 2020 23:21:33 GMT  
		Size: 145.2 MB (145154200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.8-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2c27ede8c07f9fd65f3737a6548d7d0936fb6809e155ac3e2694affcb5df619
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1c7e505088322f662ceda52329d7ba40d18d0f1ee0116f64fd3309cbbbfd09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:3cfef9f3e00105236a1ecbaa33a79e7ae89daca3f66113f0a4da3ab8de05f9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ffa3b357b53c9cf989731c121f41f7e1f51b0c496c8e1e00fb006e45060a2c2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206838882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835432d05b3b11d4ad1fa33bbf3cec5cb0c35726b52123db4baa51aaa0c8cd11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:20:25 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 23:20:49 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:49 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b279024f090539c4f61036e7224048b5d4807bd884699f33112c444a2c619a`  
		Last Modified: Wed, 15 Jul 2020 23:21:33 GMT  
		Size: 145.2 MB (145154200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2c27ede8c07f9fd65f3737a6548d7d0936fb6809e155ac3e2694affcb5df619
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1c7e505088322f662ceda52329d7ba40d18d0f1ee0116f64fd3309cbbbfd09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:3cfef9f3e00105236a1ecbaa33a79e7ae89daca3f66113f0a4da3ab8de05f9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ffa3b357b53c9cf989731c121f41f7e1f51b0c496c8e1e00fb006e45060a2c2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206838882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835432d05b3b11d4ad1fa33bbf3cec5cb0c35726b52123db4baa51aaa0c8cd11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:20:25 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 23:20:49 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:49 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b279024f090539c4f61036e7224048b5d4807bd884699f33112c444a2c619a`  
		Last Modified: Wed, 15 Jul 2020 23:21:33 GMT  
		Size: 145.2 MB (145154200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2c27ede8c07f9fd65f3737a6548d7d0936fb6809e155ac3e2694affcb5df619
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207181330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1c7e505088322f662ceda52329d7ba40d18d0f1ee0116f64fd3309cbbbfd09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u265`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u265` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u265` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u265-al2`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u265-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u265-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:3dae2a5dc0908396730bfda4dcfe898fee2b60f57eb1e828ba2ef36f977848a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2efa52f3fcde7195d000eacf1634fa86ebda581646fd1c7759b91a79b1a19ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136650003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1f7cb194a52a42f38501218bb5299d331d8195394177d9c81ffcf595f72a5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:25:11 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:25:33 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:25:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f51e19011061c113d6bfd461441b1159943dc22f4c21e1cc1676e205639fc8`  
		Last Modified: Fri, 31 Jul 2020 01:25:58 GMT  
		Size: 75.0 MB (74965321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b42002555a4abc2099e70981797dbb57b18a8736d0126bec64efc3e36d5b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122200205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3323afebeb51906690fc93a8834f665534b5ac7677a3a5437798d38c7ccdf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 01:39:37 GMT
ARG version=1.8.0_265.b01-1
# Fri, 31 Jul 2020 01:40:20 GMT
# ARGS: version=1.8.0_265.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 01:40:22 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 01:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab74c6bd2659db42f33d23de8d2d18ddcbc02aa6a0efc16bb768e284ee9bec4`  
		Last Modified: Fri, 31 Jul 2020 01:41:01 GMT  
		Size: 59.0 MB (59036423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
