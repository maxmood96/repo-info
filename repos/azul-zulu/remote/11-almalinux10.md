## `azul-zulu:11-almalinux10`

```console
$ docker pull azul-zulu@sha256:2a04a0c9d3776556404ff14213511e3fe8ae4e9e137fa2200fc1d12f47b6c963
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:79d86b84444e5a55fcee5084c61eb5181d9b724c0dceed051bab668b16168dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216472984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c4cf7169b6d00efcb8c8c7c70aa5609820811f527bdcd89191e0317e569399`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:18 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:18 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:18 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:15:18 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:15:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d77ce4426209cc3652773e46ac7d66313149619b44e1e850a6e02fa1ffc2268`  
		Last Modified: Wed, 20 May 2026 21:15:34 GMT  
		Size: 148.0 MB (148016382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d61fbff8a1cacd691be9662fb7e3648b8dce25d0aa1c193aaa3cafca9eed956c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0bf57440d69e3b3f67a4d09bdaf7fa94d560f0df6c021bbf20ff1f2d46649`

```dockerfile
```

-	Layers:
	-	`sha256:35e669ad4de08c1731c240638bd7ed7066fbd83c6fbd3cb6e43443ad50b8d689`  
		Last Modified: Wed, 20 May 2026 21:15:30 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:73522b209ed8dad9a936aa8dafc7d604eaf4901deea1f7b4ad33b2fd549b4f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 MB (214680413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6d2efbcfc4e462f9dc7e3fd980de3ef50989f6f25a1b6627fdadc5af5f9161`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:16 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:28:16 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:28:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851381fa892e9db3e542553be74bb719050df19e402eaba979f19d14246c272`  
		Last Modified: Wed, 20 May 2026 21:28:32 GMT  
		Size: 147.7 MB (147710244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c4fc4432a7dd044cbfd16a6c6ed4d1bc8bbae194379ffab048961e41a60881dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3a8cc4a1e1ea1fefd0d95c645895c4a667de60cb096eaf276ab7bbd60d51e5`

```dockerfile
```

-	Layers:
	-	`sha256:4429c5634a21f9a14c7b5e795a0f93abda35df236fb32467d9b401c9b39e070b`  
		Last Modified: Wed, 20 May 2026 21:28:29 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
