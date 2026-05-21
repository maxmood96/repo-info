## `azul-zulu:11-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:f0f988a992fe871ef1a3d5732a6dff5fd4ffd1371219ea68e1aade6b93b00981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d6ae7a4cf757e6ac00fd601a9cabf8899b0748a0f8cb21f113051937b6faff90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134874519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a808fad180a3a9ce6398d4fa3069fcdc65e02b63b47b84ab6f3a204b2c8ee10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:24 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:24 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:15:24 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5de093e8ef86d78368b7bae06ca8af3eb23cfcdc514230ba3d0149fd757b6a`  
		Last Modified: Wed, 20 May 2026 21:15:36 GMT  
		Size: 66.4 MB (66417917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:953bd3fbd6220f00b98d31373f6b40b8774e35fad99bfcbc736ffa28cd8deeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dd24ce5aec06dfbdbdd69c989868aac49462fce059222c1e2eae2e7b6b733c`

```dockerfile
```

-	Layers:
	-	`sha256:ab7a449b7f50de3db740df1f23b27c4f9a415745f0194cb58ddf4d1a2bf2a38c`  
		Last Modified: Wed, 20 May 2026 21:15:33 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3fa8bdcdb44115098c39175909f20cf4f82e47ba2fdfcc92c07d9c8fd40765a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133208933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ec04686231f0ce204809129e0928f4af35c1b5743310f4d03ffeacd8e2ab7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:27:44 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:27:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:27:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:27:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:27:44 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1102a0a56def8b54608f641ad9a7b1cf3253c8d543acffe4c037bbf7e485285b`  
		Last Modified: Wed, 20 May 2026 21:27:56 GMT  
		Size: 66.2 MB (66238764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9402b587a5b9c8eb2f4d169b0e7b1fc009fd442af81f4f335b3ef6d36cec73ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f369b7b3c9115e35f2acb8a27a7214da33e6ecacf0aecf335b55ec7df45666e0`

```dockerfile
```

-	Layers:
	-	`sha256:8cfa9a7aabf9728d11d81ee52e1a28c156d2f6d90cb4974a3085fa32fb9624e5`  
		Last Modified: Wed, 20 May 2026 21:27:54 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
