## `azul-zulu:8-almalinux10`

```console
$ docker pull azul-zulu@sha256:20c792434240851580d05bdff35ed80eb54cfec16eac6a05fbeb29f3da3df9b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:4e911bafa39a325a517c2e527295d976982e12cc071380de158ef24593b9a9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132118452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15115b374d8d8e7fb830d01e1ea60a7a049b12a4026aa6f2903292a97eb903af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:20 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:20 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:20 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd91a4af5f61067b599b0daff2dd8e424a4201d082070edd525993eaf24a50e3`  
		Last Modified: Tue, 02 Jun 2026 19:07:29 GMT  
		Size: 63.6 MB (63555990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9d1d460c41aaf7d738572d6da4fb7ddec8323ad585e7bed018b470163c4a52bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914b52a3c9fbd7898875a4eb8915f535cd070d33b1e01ddc431b71e9a52da53a`

```dockerfile
```

-	Layers:
	-	`sha256:4088dbeed6dbee94fe096e1038d994cd874c02ac08277b9590e91aa248e62978`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8882540268e65f200a37aee84d898c7da0acd58dc4528a0d93cfb7cede2072a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140710285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ba16dc9b19d77322ff73b741d5ad774d0a5e1c84b8fd0f04efa3ee6767766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 02 Jun 2026 19:07:39 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ab6b069a34137a292312841c5568c9a8ce7f14a0e8758b86aa4149413f0de8`  
		Last Modified: Tue, 02 Jun 2026 19:07:49 GMT  
		Size: 73.6 MB (73568324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c14b10c0a062007cb633e56006db2c0fb78e804270c6ebb66d8f3d7541ff29d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05400e8d47c0fddf39fc3c312deff5001b623042f5dc05c5f1e17850acf80473`

```dockerfile
```

-	Layers:
	-	`sha256:b23d0778039d4a428eb270e61f6b754480735dedd329b30d4d7a882f477751d9`  
		Last Modified: Tue, 02 Jun 2026 19:07:47 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json
