## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:cc5af6b7df0e0bf2f5952dd53fdc90e011d33c26e31c749357227808dca871d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c9edf1a30bf6cdbc9576bbd0e7684e513b18a3e8475b8225127b6450c5e8c319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228555235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cf4caee4dad4a8424c011984678350ab7d87df4a86331adb81c98f66c75aca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:41 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:18:41 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:18:41 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cfa01f6f50186ff951fe8a5adec9b1754ff3c7f4cade9ab86b8404fb53c876`  
		Last Modified: Sat, 09 May 2026 00:19:01 GMT  
		Size: 165.7 MB (165695497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9db24d35490da89eac9f1084dfca84bff4bb030fe00dc1d5b6d0c15558a5adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ff72e32755f00dfdfa28056674b65244648622ce39d6391fd4405b846598ff`

```dockerfile
```

-	Layers:
	-	`sha256:bb08045315dbaf16711d143adce66a142b73cc4fd699f0b84da92236390957ef`  
		Last Modified: Sat, 09 May 2026 00:18:57 GMT  
		Size: 5.5 MB (5536520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd32612c36a1b630fc95b6312f43cc768d8feeca26242b86d1afe7254e05c78`  
		Last Modified: Sat, 09 May 2026 00:18:57 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a3e755caf32b37847b08ef8cabebf796d1d0a258ed8ff074f9606dfd57cd63c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228716902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9662db8990c48aa2a336e7479c35f228222fc0517490f2daefedf2c56e673c72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:16 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:16:16 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:16:16 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f87a0855aa50b62231df0a7450bc85e3a796b7e5ecb8e320d2afeb62f477b5`  
		Last Modified: Sat, 09 May 2026 00:16:38 GMT  
		Size: 163.9 MB (163907987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fde304e2fb963e26635ccd1291e318b506ee768c4637b5466fb3d8ad97a93ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30018908cc0c64fae1d4c27b96060a52707a38c269f6e5867be2d00c3c946b4`

```dockerfile
```

-	Layers:
	-	`sha256:b32d259555a9b8f9f573059ce3ea4fe08e425462e34e60bc62a12d1f9325f33d`  
		Last Modified: Sat, 09 May 2026 00:16:34 GMT  
		Size: 5.5 MB (5535209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ac3393aeb6476e15a8519ec7692c7b8fc3da99431fa75e520095c8773d0ea95`  
		Last Modified: Sat, 09 May 2026 00:16:34 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
