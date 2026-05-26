## `azul-zulu:8-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:01a0c29411a2cd591b53fa6c43f313fbe4cf9f2a7ff866185ee8b20cfac74c01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:25a6c532d8693babc4f4642f4e1bd7d537fbdf0b8d98d6e8497c13bc3c6a200e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119709306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05df896c296b4ec7cd0838d3ab77b08413a6d2f58a1bbe525507df20db7fa8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 26 May 2026 19:17:39 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4b143a5e233eab6970fa4c31d79ec8993ed52e06e714e1ef75079adada0b31`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 51.3 MB (51253269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:dae358cc875f19e4d4b1709fe68ee2e9611dd50d6dfb63a37685b5e45214ef99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8b1930337cb9ecfc608c1bf12e16d8a4e15094f5f96f323d3234ea86a5952b`

```dockerfile
```

-	Layers:
	-	`sha256:777fa5a76dd01fe43760db6d13730c3ece03b110b5cd5d733bdd6e410a3edd76`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b4ed6d5caf023ef23c4b59f2434c39f302d9ba6962bacac4bfaedcf34cc3ced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126503714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a766b25f2186a1b444a4dd882c3878908da76a9f620b09fe9d0d097e7333c`
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
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
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
	-	`sha256:dd71f9ca01cf126df4b358e9b7618e469943f1960562a7a58d2278ec4f1e995f`  
		Last Modified: Tue, 26 May 2026 19:17:49 GMT  
		Size: 59.5 MB (59532822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0182661dc1662b1eab7fb707e4ebebfb2e7d66366b0e401eb52b0b4b5ffd8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919c9d9da95231bc201e623fb44b2126596720bb88c62b81d54921acce68469a`

```dockerfile
```

-	Layers:
	-	`sha256:f20bc46c7f0fc8ce47fa43fc6392c7a1d63104a32ccb80a44b404359cbdcc17d`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json
