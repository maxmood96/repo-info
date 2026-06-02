## `azul-zulu:25-jdk-almalinux`

```console
$ docker pull azul-zulu@sha256:527cc9a51f10491164e91b7ea4051f311e664ab3fef07b99e070431451410e6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:949856d281f6d90ec43d28ae98355519c218c3461f789be17732e00211d5a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253041162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d624c9687c14b6f86fe65292ccb0d8d00ca0f5662fbcc7b58ffb0c4513ef93`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:22 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:22 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:22 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b8ae91d5eace59ca8d22d08c253a523ee17501e1dbee9958c7db7da6a69c0f`  
		Last Modified: Tue, 02 Jun 2026 19:08:40 GMT  
		Size: 184.5 MB (184478700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fad818a883f75f951fbec054f2cd6ef3462095b5238f0877466173c6cb6e1775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c2964df767d03b7061b102b8f26aa57b73f623bc192260fba42a28b1e2bc7`

```dockerfile
```

-	Layers:
	-	`sha256:ca5225f584a3cd7eca9ed295aff8b1f1afde649362ad246f293c3d8d8d9cba65`  
		Last Modified: Tue, 02 Jun 2026 19:08:36 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:41de91eed3f3f2c8026f15d55abd19c5e24f93f1c8135e9a78ef0f60dbdab224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250774594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbe360a52455914c231b118665bad6dbbd610fdb8c0ae6d535f28acd6ef60a1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:40 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:40 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1ad22edda6b4aa130eef616cbb6dffbac638dd2ee064ca0f0bf5cd43605118`  
		Last Modified: Tue, 02 Jun 2026 19:08:58 GMT  
		Size: 183.6 MB (183632633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5dab7379ed0d4603d4beece39ff12a713eff28f28ac985cb69b64cdb63f46b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea27017975f345746b5e1582b31c9bfb5ffbe6b93dab567717dc1f34a4de398`

```dockerfile
```

-	Layers:
	-	`sha256:bd635fbddf6d4de3cdec558edea51923d0e012b5c9c76dbd0b510d38211461df`  
		Last Modified: Tue, 02 Jun 2026 19:08:54 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.in-toto+json
