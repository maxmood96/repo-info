## `azul-zulu:21-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:45baf5a3c3db7167b4edb029ec3a3cca112be70c56caa7c81780077b514b73de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:db858abe97e3715f2c1abea55f57256a25e34497cf28f4bbdc6623f4fa037c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144654938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc483db518b8896af85df60ce63c545d9facad711866f107990df378afb3932`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:21 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:21 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:21 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c5f59fa9c6a2899cf650cea8dda58fa9c2283737bd2cc52f4558fca2862065`  
		Last Modified: Tue, 26 May 2026 19:18:33 GMT  
		Size: 76.2 MB (76198901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:78714b2c77b1f4c893c134b30f40a33fe601d75fcc01171edcc915847a29909f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02900a6cdf5e6bcb11d563e226433938967ae282e8046019ba63817b8b5e6be`

```dockerfile
```

-	Layers:
	-	`sha256:9b5cdccadf510f1ee62b29d16d0260aee333e7b1f075ed34bcbbdd45d586dfce`  
		Last Modified: Tue, 26 May 2026 19:18:31 GMT  
		Size: 9.1 KB (9140 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c0128b52e6c4d521fa79a7116e7b64e2bb66f95c8adf48a052bca20278d51af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142835834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49cbb495eb18531485a050e7dcadf3deccb026004cccdf5cd86db079d200b19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:32 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:32 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13046b4ddd0cd5db9fb7db373b796416555bc5b4e91a31bcfea323782d1aae9e`  
		Last Modified: Tue, 26 May 2026 19:18:45 GMT  
		Size: 75.9 MB (75864942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d9d35bd9fafdd84d4a9a6de16ec191be2d3adff6c1065ba641ce4d7b07d005e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70694289b6093a0e639e8d9162a4509eb7b36d16ef28a1c2a2f7ba8113ee6d38`

```dockerfile
```

-	Layers:
	-	`sha256:b8f9ed8383c47b72df53c53106ba944e5d816689b089c548b994624cc0c38e63`  
		Last Modified: Tue, 26 May 2026 19:18:43 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json
