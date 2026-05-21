## `azul-zulu:8-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:aef6050b688fcb1d95656935d2096222575a92d1d02c7d4d2d2e2d45b9a1b29a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cb4dee6c176b2d215df0bf3bbf1a18d2fe7e283868ce49c5a43e6a1ce3d0f464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d320b5c5bfe0a0aa3d49e30862aa79620913387d911b828ad19619c6500cc50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:14:10 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:14:10 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:14:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 20 May 2026 21:14:10 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e5d50ce6f4f379988fdcd0ae83ab5e9b0aaae1e04a3bef5dbf82b5dcfbd4bc`  
		Last Modified: Wed, 20 May 2026 21:14:20 GMT  
		Size: 63.6 MB (63595206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1e24df167dfa495299c390bb3ca21f45ee4fb028b14616ab3e83b33d8e82d0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91fa9cc989f78def52f6dbf4f35353512f06a83bd43ae045dc76a3d957ac9ed`

```dockerfile
```

-	Layers:
	-	`sha256:541f49d126c16464ddbd402b2cd44645ac62114470775788e39c4ccd407d89b2`  
		Last Modified: Wed, 20 May 2026 21:14:17 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a092eedc8c7119549c5d7eac9eb8b7436e751b55e9715863fc5e2555c39930b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140579320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f589154f4d3264893cd9dbae5bbc14a1bbe14ef20f585abd9c505d002d234ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:26:56 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:26:56 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:26:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:26:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 20 May 2026 21:26:56 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563274fb4a15f84419efdc7f8843a1dfddf3f326708b6e3de378b0d3d1e009e9`  
		Last Modified: Wed, 20 May 2026 21:27:06 GMT  
		Size: 73.6 MB (73609151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0c4c0bc6473232664aec02adddbee43b5c7b657f33634705f0b19bb178d7b4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1470e6fe0666b073354d1df6cc75137464b4533b47bd9d577d2e44127f2e0ef`

```dockerfile
```

-	Layers:
	-	`sha256:2680754a6a3bb16e4169f10b302d5e059e71b3d26ebc4f21e2e6ce3526956f22`  
		Last Modified: Wed, 20 May 2026 21:27:04 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json
