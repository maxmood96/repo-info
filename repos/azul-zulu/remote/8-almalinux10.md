## `azul-zulu:8-almalinux10`

```console
$ docker pull azul-zulu@sha256:184376b4bfa7ab95788a0c9b2a50057b69198d44f714625e552d0489100454a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8d40b46e3df0e9b5aaba266d49b3dc1cf4e9b61f34a6d806718b5670638baeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132062354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2688a44a47cfbeff7576611b7a4b397d17bb445e1afe6f8003a6429143268e74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:34 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:34 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 26 May 2026 19:17:34 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8588a5e5a2c3ccb49eae23184149a1c0a843398a01f78775724bdfce53d39a`  
		Last Modified: Tue, 26 May 2026 19:17:43 GMT  
		Size: 63.6 MB (63606317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:83c14731fd6ae379d31b589534dfe627b7c313aeeec297a42cdb7776b52b0f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0c53089602282276cb68c48d70c99182c46598a2f94b87c6ce89d6cc80fdd4`

```dockerfile
```

-	Layers:
	-	`sha256:65f95e57ed83cff131805be92e9d93a21b353ea8c6b71cf03e123e5b9bb12a13`  
		Last Modified: Tue, 26 May 2026 19:17:41 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f6735b621c09ade7c6e7dfab56c4344bf732ab43bcd8d9644fc91e735dbeff10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140591485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e83676734e03566d737ccd9db71b72e260699b9ddbe7b3a26f647940cd4b33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:40 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:40 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 26 May 2026 19:17:40 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b5960b5fa0016638726f15f64a2319341ebf8710193bebbfbcb03ff033473a`  
		Last Modified: Tue, 26 May 2026 19:17:49 GMT  
		Size: 73.6 MB (73620593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:86b9dace019f7f2901289e199979a4c53ca2fc46b2527d991b369cce900f2f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fdbd1e26f465e9f1ce5582c2862dc36c42c03b28f1d03d0b5c0f5766859f4b`

```dockerfile
```

-	Layers:
	-	`sha256:11ad9222f15f0e55380783dbca75920a04997c0b837c175cb41bc46e9175185a`  
		Last Modified: Tue, 26 May 2026 19:17:47 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json
