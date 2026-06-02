## `azul-zulu:11-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:7321e93f87e359eaa827bfb12ce4d5a1fd2a5c2a8f2f088718aad41ecd48b6b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2b92ce847d0cce523945841537393596d8fcc1f3890367808436c0d6afe41b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215688998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38429cf7176fdfbc8c83506a96ceee624dae4551203f9d799c05539d1f9b086a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:38 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:38 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:07:38 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4065feeed4397a66be748461373ba04fc2a9df64ef57b6d108e9741813b1b9e`  
		Last Modified: Tue, 02 Jun 2026 19:07:54 GMT  
		Size: 147.1 MB (147126536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2c2a84ed60f01dbec7c67b4946521ab2e2c883bbf9fd1a95be4cdb5f33466b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d40c2b57cb517944817f4f3a6d2ccc3899aaed1bf299666f92a681018c684`

```dockerfile
```

-	Layers:
	-	`sha256:9e35cb582127f44e65ec07fdef4f7b33cd8f76ee22c78e46be27ff9c297cd9ec`  
		Last Modified: Tue, 02 Jun 2026 19:07:50 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:68d6dba6ddb046c8718dd9b82aabdf2bd3ef8d16db12cb3a2892e08497760c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213954238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab5a93c2a6cff966196d5e004fbfc869ac5242f6633088b4e4ea63024c076ec`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:55 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:55 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:55 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:07:55 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2e804502a725c11fcb0dfda489df94c1f1d7a9390e97a6afb801774c84c79`  
		Last Modified: Tue, 02 Jun 2026 19:08:11 GMT  
		Size: 146.8 MB (146812277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5ec0c4f289f38d98ee264af009c57eca0e6f5cd5fe1d5182ace8cd5a992252a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa6e9b2c3e32af2baccc43882ad0628e377571d6e88f029e9cc344d792bfcfe`

```dockerfile
```

-	Layers:
	-	`sha256:420886bb7ea02d98dc0a546aba1077200eedd3cfca50ca6bfbf5f8827fb44929`  
		Last Modified: Tue, 02 Jun 2026 19:08:07 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
