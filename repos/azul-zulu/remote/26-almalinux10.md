## `azul-zulu:26-almalinux10`

```console
$ docker pull azul-zulu@sha256:d9086e2850b347727ff59ac4331f218d90251a7983ee5d35bb00143bff5e5a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3640a398ee148f3ab6d8a70ed72d20a02b6c0fba8020c95388f10950f25e00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255314961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bceafefeeb3e261569d79f8c0539414f3362683361b923d6bd694e0d33bb1f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:35 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:08:35 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4737a009d77854833cb441983946c0d85596dcf391f026ce3903bb7700cc988`  
		Last Modified: Tue, 02 Jun 2026 19:08:55 GMT  
		Size: 186.8 MB (186752499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:46f804a8e136189ab473f12b1a71df7043b6ca19fba20ebcea3c82fb720b7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067535d161a39288af15e2d27b48f660a839b6ea3f4717756f55a4fae35cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:140fad3147b04fed863bac88250b9ec5db93c34be6a3c3e5f86de999087f2d3b`  
		Last Modified: Tue, 02 Jun 2026 19:08:49 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ee76f747717a7681c4800c36aae7d0c2b80d1cce1820467d3a03a619e0441b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253599165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ec93019efb63d877c7d2e658739c9eac8e691292ff89474baea4e8e68a9aac`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:09:01 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:09:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:09:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:09:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:09:01 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:09:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f671315fbb38b5e412033cd4b9fbe6b5e614a5759dc3a7abcab28e6439ce8dd`  
		Last Modified: Tue, 02 Jun 2026 19:09:22 GMT  
		Size: 186.5 MB (186457204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9feff305bbf30bc77b7f900f817eb55a98eec44a19e12692d52c0fdc33f2219d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beb7578724d97e6119b03132a8164cf2cd939df4ac113fc99a0c859f1a59a8e`

```dockerfile
```

-	Layers:
	-	`sha256:d6e618633e806e3daa6a0c21bcd6a024ce1b519f6e1b387299e98fd873384dc9`  
		Last Modified: Tue, 02 Jun 2026 19:09:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.in-toto+json
