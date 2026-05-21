## `azul-zulu:21-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:1b22e3c0b76332b23afadf227906a3ae0d1667977df0793ca7ad426d2f38a107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8effd732cc3f2f69bd112d9045a157daebfcdefa26cc91616638797f9baf3fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144657239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5874222e0f832d3c8f20aeb09d1af3c64c02138d4d1b8af19122693efb4a1d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:15:32 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84681173532e9c0906c2ed1f57742eb49d19a0a472b90cee7caf8fd33788d0d`  
		Last Modified: Wed, 20 May 2026 21:15:44 GMT  
		Size: 76.2 MB (76200637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a71222fd3a33eb4b8391174c9abeff8040d838311fad833f27c883ea1a36acbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6d71b30453f3a61aff8203e99abf2ede3e43429e75416bff466eb35e25d91f`

```dockerfile
```

-	Layers:
	-	`sha256:ee453914ec0539c58cdac2a000fa08337aafde03bac515b4b75b552afe867563`  
		Last Modified: Wed, 20 May 2026 21:15:42 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:bb2d6fcd9ae28f7db4768d532126c9769d62b7582cb44790a40073ae939abbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142833057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae1758daf6bcfb5f108246b6f877f95132d61041a2cb737d5e2399fc465f2fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:19 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:28:19 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe070276d725ee0d030248669800ba34390a547537e02997e2e9ea5ef4b9dab`  
		Last Modified: Wed, 20 May 2026 21:28:32 GMT  
		Size: 75.9 MB (75862888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0f6757738a025fec6385b9b540f4283355859b8b2e7d97e3eb272e3dcd154131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187c6d9597f8db448ff7df8d7b97c956263f507a090d925bda868119dc9415b0`

```dockerfile
```

-	Layers:
	-	`sha256:4be403e084d72832212529794315d898776a4a2856c4c9f5eb3548daf20a1412`  
		Last Modified: Wed, 20 May 2026 21:28:30 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
