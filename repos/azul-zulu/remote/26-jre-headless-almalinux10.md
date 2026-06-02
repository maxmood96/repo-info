## `azul-zulu:26-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:2e801eb193c15d1c8dd48802ca3fd4b80c697c4b7f17feb92e530076e40e3ae6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:bf3e576e72035574961647ff404da462cf66d4c46916035c14b2a164f985ebb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159586594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0e7cafa55d13876d60f9dad5c0e418a1e6272412240a5b230784ae53352c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:40 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:08:40 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d0375dc63cbb8ef71abf82c2481f3253407bbb01a4b55ac2e98c7eca69c25`  
		Last Modified: Tue, 02 Jun 2026 19:08:53 GMT  
		Size: 91.0 MB (91024132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a7a133621016a4be790bdb837f0fad9e9ffa860207b244df010b49b96d8b6322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b605bbe5e1425f543819d34c110ef0a7b4a72a82848ae8667615cc3a898326`

```dockerfile
```

-	Layers:
	-	`sha256:2c6e6ac0f9fa8218ad9a269920bc6998f419e2659be72d2064e096f93e95f66b`  
		Last Modified: Tue, 02 Jun 2026 19:08:51 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:013485db62e0f8959eb73ffa00fbf9d2c3a400bca77a067309968a9be809cdfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158090757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9879f430f41a019a018371e00f56aa087a8f6822ed80a7b7a65c7be345d4c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:09:04 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:09:04 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:09:04 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:09:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:09:04 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14bef68f870c2131106a6aa8ef40979568380826d497651ff901eac1bf31879`  
		Last Modified: Tue, 02 Jun 2026 19:09:19 GMT  
		Size: 90.9 MB (90948796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:186b3e3e5c0dce4822c935ae70294b2040708103eb5f67e9bb3d2c1146463b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03810c89c822ccb6262b468ba8faa4e7a03a85a66d8a5897982558b57fec9daf`

```dockerfile
```

-	Layers:
	-	`sha256:2ad289a895c64dda3292937824454df0e7ae0eeead7bb6078107ad69a5d691fc`  
		Last Modified: Tue, 02 Jun 2026 19:09:17 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
