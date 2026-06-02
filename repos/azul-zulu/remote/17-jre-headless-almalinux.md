## `azul-zulu:17-jre-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:eff6f7bf26963e96b0e61c7e58bfd639733e5a5fdfac906ad11ce0af17787510
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:e0dc8a1434421b04fc971388de6f721fed35bdf5819b23eda6de383c485632e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138972865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07e3095b1a9660c16449f0ebe85032f2de5c4b13030bb2d849d491286007498`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:58 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-headless-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:07:58 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5914a76daf9c3a75e0775e4e892002cc6b07642b11def0fe2f0d32a68ae53`  
		Last Modified: Tue, 02 Jun 2026 19:08:11 GMT  
		Size: 70.4 MB (70410403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a39672fb90d1e474a2191fd349c5c4399b1bf9f8bc0157fe21b5c5f2b2e8dd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9842b8d1ce987e4f4740ad4f3b7a37bcc0b5759d03b495bcf68a4bfc0c53ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:f30d4a0ffef1fe2c4bddb05bc55122acae9f117d01e74504711541cf4764d832`  
		Last Modified: Tue, 02 Jun 2026 19:08:08 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:aa225fe7059c85d3a54e451e45a4140d86604dc55391bcfcccd58a5bd3b72972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137612374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422750eba70cadfeb3ca3addf30244508f6b6406d63b25d35ee005ef1072e90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:23 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:23 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:23 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-headless-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:08:23 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699b58911370b2d9deacb5ce6eab8cc25e4a50ab4f3358742f6a1e6b21998f97`  
		Last Modified: Tue, 02 Jun 2026 19:08:35 GMT  
		Size: 70.5 MB (70470413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f0699c653bd3026f303954cbcfbbbbf0275f6962c76a01ea1a9efc957f7c29e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c6694194b4eedad77b61bb1df0e74be82a510f806831d2c388decbb464dab5`

```dockerfile
```

-	Layers:
	-	`sha256:a113041f204a0922951d66224d57e00c17d3d22c2f448506d85782e3ba5ca742`  
		Last Modified: Tue, 02 Jun 2026 19:08:33 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json
