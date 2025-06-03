## `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:31db762207af1b4a5bb43c6941a20706fa46728eb9c90fbbc8565be9779ed1b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:aa8743b2ef850539866565c4a046e0c8e5f80f0e284fc9b508d754a581cd2078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287118530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62d63c8f6f2180774db8da130a939597b34db376bf969887a132f24b5bbb216`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320753fd20777ee40e9178f35d9debcb6e06f4d9b16468ae9463d0d4cb84919f`  
		Last Modified: Tue, 03 Jun 2025 05:16:33 GMT  
		Size: 157.6 MB (157634484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda9780b5dcaad7e90c7d0dc1861000ba42fd8f0d9e613cf335885aecde4a74`  
		Last Modified: Tue, 03 Jun 2025 05:16:32 GMT  
		Size: 81.0 MB (80994763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8b719f8ec5f897a6a544c34ca08adb8268bf1d32c2319fbbbb613e74acbbb2`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036a55dafd31ccc2a0c4a4a09b3f5d9dae8fb84741a9a01f76c925b0d25777f7`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0827f6e1323f2fa7b5d37ee54e3686e94fcab4c7349edddf98567f6600eaa022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78c5f2d8a8999bff261919e4f981c063311afefb3b985674ed75e2f1379e765`

```dockerfile
```

-	Layers:
	-	`sha256:d380a9a4708c293a45f9e2de13aca76be4bd645e3b681ded7ad5e85d1e7677e3`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 7.2 MB (7223624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f222828fc20a17df78fa93f12d0c1b90b0f3c8c7c451a97214597004ba0efe`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03cb0dfe9efd242b8f63b3ac0f21613a12ef6d2cf5fd16d11806dd7691b0e102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285103987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a072c36b1bdc7c87d2965c86be60905f1bd36146487c137eef3eea35094959`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f670fcdfa1a1eb797188a5b4ca5053a8314031c8c9ccafb10f28c17b8a14294`  
		Last Modified: Thu, 22 May 2025 07:59:11 GMT  
		Size: 155.9 MB (155928835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f10cbb3e519a9dd78d7659ddeefdef904a8dc2444280ae4e30c178f931da7d`  
		Last Modified: Thu, 22 May 2025 08:34:17 GMT  
		Size: 80.8 MB (80846930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ec04a8a382772611ec75f31812cf134119972c8893cb41c89b35191f5db646`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee410f678ccf2cc4d43a56c85bb0091bd05c63fe636ea4480b2050d3314a7ed`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:94152a273395c5406ee9cb2f9bd09b2927bc0cab261066c5b50ae1ec159c730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771225bd5990814e63299691bc856a81e5ca0a9fc39ad7ff0f1c175aa866f80c`

```dockerfile
```

-	Layers:
	-	`sha256:c44363d35a22682556f0ac86c6579753aee9dd51fc5520f17dcfa50c9506da68`  
		Last Modified: Thu, 22 May 2025 08:34:15 GMT  
		Size: 7.2 MB (7229459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3aef58842b4d74672d0cdf54a441c60c0156c6f26a72344124cfbda6aaa5acb`  
		Last Modified: Thu, 22 May 2025 08:34:14 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d26aa43639c73e0b91a13140336d0d2f9ca53edaedda0df90086301178f2aeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296948111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17bd2a1545f2d8b282dd9c08cf7b3930da47386060f697b7018f22dc060a9ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f3e50388b64ff117b3b9106a068a9d7d13c6cd1faf4e5eb6b819b11983c6d4`  
		Last Modified: Thu, 22 May 2025 10:34:39 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7aaed8168313f0215e0152b44902fc771e1ca8331ab9aa70e73b4dc3f5324a`  
		Last Modified: Thu, 22 May 2025 11:34:51 GMT  
		Size: 86.8 MB (86810546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629242b8086fb6f34af97adc7794f0c17d044bc343a00ab5e2de4ec0e42af0e`  
		Last Modified: Thu, 22 May 2025 11:34:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f945a1630fc088f9c507a14d990c3cd52e81499d5a0712da5c8f9b1c691857`  
		Last Modified: Thu, 22 May 2025 11:34:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c2d41c66eb05f3932340b50c8c59a4ee8e81a0cc8ef9565f17b72a53cfbe0f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b071de4d1702ef58c029f962a668fa42753e28ef78dff9c21e5b49f83aeda129`

```dockerfile
```

-	Layers:
	-	`sha256:68777416ca4a4adc3daece2d7f0685877f58ce90a89ad08c2841ea9e03667ae8`  
		Last Modified: Thu, 22 May 2025 11:34:45 GMT  
		Size: 7.2 MB (7228864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380886065168326b776f03bb4d87e47dc2e95459ae18f09600ce6b22dacde3b6`  
		Last Modified: Thu, 22 May 2025 11:34:44 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b46aa39c0afc739197493ae74f36384ffc6a6f7e5d27671b5faf43e963308ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273845873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba67866234cf4b0e338cdba880ad706db28b29b7eda9976b4bc2187e2731d2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f7f624f9251dfb21473d25e67300bb9a6b55ab2e666b7bae6f6bac57d4456b`  
		Last Modified: Thu, 22 May 2025 03:37:38 GMT  
		Size: 146.9 MB (146910901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3647f48d61b24c50c3ae5ea62903620c0b19d0054d7e63047c4cd50a8bc4fd9e`  
		Last Modified: Thu, 22 May 2025 04:01:31 GMT  
		Size: 79.8 MB (79790091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf05c14c77bc058c21f858c1a1d189b72cba0a7cb3f9beb81fc39370cd189e7`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9cf1844c802b0b6d329662eafaa4467c40d9695bc045189dff29b73c4a60`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a756c68bec3f3dab309ecc5b4db0961ceb8298838f5124e03ae09118861aeb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9c20c3088d890fd72dc5452e99e8014ad656db302085e2622a4fcd68699a53`

```dockerfile
```

-	Layers:
	-	`sha256:8577843467f779943e13719c99cb3d1ce18fbbbc249389b27030e3c17a4acbbf`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 7.2 MB (7217835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216b9466632b94e04aaea541f2456c6b18e6e01bf562cede591fbded3a38c9e2`  
		Last Modified: Thu, 22 May 2025 04:01:30 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
