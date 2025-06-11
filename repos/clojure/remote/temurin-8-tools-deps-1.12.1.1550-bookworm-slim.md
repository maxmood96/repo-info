## `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:7a977a993128184a777c24210c4274ffdaaf013384f7fcb65ca96af581a593d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:227fc947602e3e6c4acb6b039cc5f11ee8bfa632a7e7ce01b52b3403edefd525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152476796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6d54de45dcf267394b826d30a4d7c1a4410ecdd4453bbc21e602670a38501e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ecd5cb5bf3bca9f126e23505885df38d47fd61690fee5521dec4414c49913d`  
		Last Modified: Tue, 10 Jun 2025 23:50:05 GMT  
		Size: 54.7 MB (54716158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23bd6c57b0f4d272b0ef631c138e10b323774505041d10b73a71a77c253c152`  
		Last Modified: Tue, 10 Jun 2025 23:50:07 GMT  
		Size: 69.5 MB (69529864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb155f5589091c85d72a299ed2d51fa5ec2150e6144d4ccd981348129029a0`  
		Last Modified: Tue, 10 Jun 2025 23:50:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b0e67622b6037900c8ef5a7980ea4738d2c4047a7f7fd698b65c26f6f089908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9e48f0c2ad2bd09b1f8ffbcceeb1ffe5c3baaf381311d2ccc12398740f6f38`

```dockerfile
```

-	Layers:
	-	`sha256:5be52accb2580e42778c3d939ef89e456ba1177b5a73b07ad47ede2379e5f507`  
		Last Modified: Wed, 11 Jun 2025 03:41:27 GMT  
		Size: 5.2 MB (5231498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c667556662c4f8d7800246981794dde59c80fb9fa62b385845e93f4a04f005`  
		Last Modified: Wed, 11 Jun 2025 03:41:28 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77dfa39740205877998a917f7e53791ff9cd6be399324c8fb522a7ae8a3fcc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151287453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f8d0bd30906c95b5fc9c8c624a3fe1d31f658cc78a311581c8d5b21d85a54a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a417e3b74fbb7215b9587254b3c223d093abcb78011dfafa76141304d521fabe`  
		Last Modified: Tue, 03 Jun 2025 19:24:40 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1beb34f1cdbb61dd33a255ae7b4fa90f8910a53e52cf34b4d34429069f3c112`  
		Last Modified: Mon, 09 Jun 2025 17:32:56 GMT  
		Size: 69.4 MB (69391026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9207fbdf23b74a9e9fe462e0f7c2a6e77dde1f65f47797cc6d6d5d2851968cf1`  
		Last Modified: Mon, 09 Jun 2025 17:32:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77eafb0d97457c98254b3e85daee3367c3bfbf99061b7905fbff3667f91ea5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1cb21dd9619af99a8d19d0471d9e46b5691dd766203626372e30e066c30aea`

```dockerfile
```

-	Layers:
	-	`sha256:c04079eb093de8b3f25bfa32af8bc0065879870c557276641a6141cabd8bab2b`  
		Last Modified: Mon, 09 Jun 2025 18:42:50 GMT  
		Size: 5.2 MB (5237957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe69d343710a65fe2efa9b5599caf79c44a6616aa5713b10f8cafba08d2ff89`  
		Last Modified: Mon, 09 Jun 2025 18:42:50 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8cb0600994540350b81f90050fda282dd0ea767231fc4e27cd71da23fd47ed39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159581274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb5afaa5c5d3809d5345eac21e8ee20ec6cb380154847f1c1c38833cc0d3e55`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69330ccadd135120719a7f8e4da60763334e15c7b37c59d3bae3f4219bab28ff`  
		Last Modified: Tue, 03 Jun 2025 19:25:00 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f81bfa12d5b30f232541aaabc1a081b5801eed61c68a61873f69fb354848c34`  
		Last Modified: Mon, 09 Jun 2025 19:11:24 GMT  
		Size: 75.3 MB (75345751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd10721633dd0bfc6e91f6d209dd95c94d21da9cb8f8af13e18d3fc746e6257`  
		Last Modified: Mon, 09 Jun 2025 17:48:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a58fe9038e7c296caa437b5bc8d4b77865f9d2b3c2c19e8fff2448442507c937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64831aa94861a7cfaa22fea903e1dee5577fc425214148167cf41c088148d1e`

```dockerfile
```

-	Layers:
	-	`sha256:edcf9aef29cf26befe16d0ce46385d3b2bb9936f9412e913ae1c978b797c94d6`  
		Last Modified: Mon, 09 Jun 2025 18:42:56 GMT  
		Size: 5.2 MB (5237249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac2ef713153f43582c591ad4a7d21abb69364dbde8ba3699aabac21168567fb0`  
		Last Modified: Mon, 09 Jun 2025 18:42:56 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
