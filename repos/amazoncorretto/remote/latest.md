## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:0d1281a79016e2148c2062f4364c1a9ed9807ec3325da633d204069b34af51bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc406ded155885da5da53b67cfb05b9c27794663d3dfc656c20d6f9ea03c04c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138459146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0defdde877065aebd9a81445928dad3b7c407e1b2bdf4f8363a75d8643cdadb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3987d930614bff608d3dd8c33d6c69acaed62e7d377df635ae7526a7136c5770`  
		Last Modified: Thu, 27 Feb 2025 21:07:59 GMT  
		Size: 75.7 MB (75657104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20527fdbe04ee0dc48ed84ce5e7586c25f46f5afefa0cc9d9dbc71b7f2932a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32287c58bc5940618194dfa1e681e2a41b0a2183a452815d4ecbfb4a74a3a8dc`

```dockerfile
```

-	Layers:
	-	`sha256:1b38ecb9f4ab2cbdbcf418499ec0896fb95fdeb8ba74d4c30f0b5632690e715b`  
		Last Modified: Thu, 27 Feb 2025 21:07:58 GMT  
		Size: 5.4 MB (5359568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5299de74f2c9baa6156475c19e797d04648738711d86ab11614b9419e183be0`  
		Last Modified: Thu, 27 Feb 2025 21:07:58 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b600bf34cb9bd5097e626cad877d10887bd65e826583133991e07251916e7de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124240847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd36ffe89f7593d436328aa9f2a97c94671c77c12e805b23bd33d51acd5aab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2841449421858c24f162dce589a7a25d026560c97714e2d9454803961ba708`  
		Last Modified: Mon, 10 Feb 2025 20:12:02 GMT  
		Size: 59.7 MB (59662625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d245c0c7b6d09d7237c01b01a8cbc1d79d94229763318c859c99f8b3e3940227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781fa8e3441867e81469c3a7f4ff93d93cac1bddc7e3cbdb6e7bdceda52562f9`

```dockerfile
```

-	Layers:
	-	`sha256:f3e58dd4eefc09d64d87d7714e4178743df61605db1811a936851ff77329f2d4`  
		Last Modified: Mon, 10 Feb 2025 20:12:00 GMT  
		Size: 5.3 MB (5338067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad725ff3087982b7784efd80e51893b2716ae7f0dd08daf5203f84ba62c3762`  
		Last Modified: Mon, 10 Feb 2025 20:12:00 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
