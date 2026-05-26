## `azul-zulu:26-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:675416f4d2413e99225cf001ac126366de7732ddab35fba08a92a2869ba74c72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d78e1020a7cef9b8cc72e19b571ec331c02df24af54ec0f2bff94c623574215d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159890814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d211f55986d0645986840c5ada951a2e2d4860aaecff0209f125f48d32755932`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:50 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:50 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:50 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:18:50 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e5f3eaaf1cea15b9aa9431e6211edf92dc2f370768abd50cdc9bff34bf9845`  
		Last Modified: Tue, 26 May 2026 19:19:04 GMT  
		Size: 91.4 MB (91434777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bc8ac19e88a4c17208c8473661dbae3e8e6725264a7f83e14d98d002e9ffb3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28daede1190d97341eb7c9b7066538452b1ad2c4eed73d2ee111d51c46e16451`

```dockerfile
```

-	Layers:
	-	`sha256:eb2e75cad91b61efc54aafafd1871ed804701637861ae897dcd220fb4c4e7dc0`  
		Last Modified: Tue, 26 May 2026 19:19:02 GMT  
		Size: 9.1 KB (9138 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:07fa0ca55094d3661f5ec1dd200e7333b3ffc8b1593b43fe989d74728e1b0200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158326358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc941e643e03852c63f74d9b5ca337ae8735d9e6ff53a07e2216c69653fa206`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:19:03 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:19:03 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:19:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:19:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:19:03 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe9a0b484617fdd4444481eec7d2a433a3cdb8cd815fbb22b480b5721b8ac6`  
		Last Modified: Tue, 26 May 2026 19:19:17 GMT  
		Size: 91.4 MB (91355466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8286cc872480403af4c7dae299994f4732525c95e0bf8196e89c8a308a3379ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e36ef00b052ae637fc25461e2c1aecaf42e2566fa078bc638bd8f913f4591a1`

```dockerfile
```

-	Layers:
	-	`sha256:f3011aec23495f9cb3f1cdd006da988cce571518bb498e131fdd914b30a3e01e`  
		Last Modified: Tue, 26 May 2026 19:19:14 GMT  
		Size: 9.2 KB (9230 bytes)  
		MIME: application/vnd.in-toto+json
