## `azul-zulu:21-almalinux10`

```console
$ docker pull azul-zulu@sha256:42804fad9b62342e8b6357d3cb4ee397741bd21c7c3831cfaad17d99209d37ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cd0c8661998dae2d6e8c4a16aeb4799b5c24af58b0257f157093abb8c02f863e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233981642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0964e97e5ed3c254530683858b9e375884e6588d03e48306af8d60ac64867d7f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:05 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:05 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:05 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:05 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9191ee16f5a3f49fae286d4519b3c2f3d7926fbd595d0d0d6c926c6162f8a4fb`  
		Last Modified: Tue, 02 Jun 2026 19:08:23 GMT  
		Size: 165.4 MB (165419180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c4e87d48806e8aae6fc8cd6673a3b6aaf0ebffa5d1fc9ef28af44e11121ec025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bda8107a0d137cc8051395d9257aab08ae82f8036be259ff85e8ab7c8a6b0c`

```dockerfile
```

-	Layers:
	-	`sha256:95b8b9080c1b010b187ff52df7de960b3416a3fd7a0e3ede6c063835cc020d7e`  
		Last Modified: Tue, 02 Jun 2026 19:08:19 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6d99335faefed1f3cd4ff13a6845f2c7651e74365f4ea2e2fb65da4c6cbc7682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231879895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68572a88a39fbc107cf22cad3fb3ac0ff9489e3c1a4f08636cb8de79c33c94b2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:30 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:30 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db267dde2635aca3056e62276d189d223bd9490d491abb5c709fd5d4e71cf645`  
		Last Modified: Tue, 02 Jun 2026 19:08:47 GMT  
		Size: 164.7 MB (164737934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:67e5c5d5c21cef5790dc0e83309d11c4bab339aa03c6c7dced0b706ddc7ffe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfd1f4ea121bdf5377192a27c5cf2342fe8e21d46e13a03c0ffc5d3aa3436e5`

```dockerfile
```

-	Layers:
	-	`sha256:8b98f3b48103bc11e07a8c6cae9418b20e8d41f60f6e4447a9b8331c68e30765`  
		Last Modified: Tue, 02 Jun 2026 19:08:43 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
