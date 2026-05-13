## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:1eef0bd98d91e1794faf999394ce84905604db227cea72feb3607cec5c0fd0b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8b6b00a09893a88a2d7844271a02bd2a8ba4cfd85b4f74c15001326dfef547f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184854532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f39b243acde129150a38eb7d365cfffd06d7970ad9d9414e9540ab0dc01fc42`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:45 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d096001dbe26ca69fca72cf4131e19571fbc355b86917807be33ccf407ef244`  
		Last Modified: Tue, 12 May 2026 21:46:19 GMT  
		Size: 55.2 MB (55198702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a68233c868bd996ec5f4fb22a449a29b68918f3e2a02009a643e94f02c73e4`  
		Last Modified: Tue, 12 May 2026 21:46:19 GMT  
		Size: 81.2 MB (81166508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ea5023396e8d7dfbdb6b96b25139fe9af9feda9281cf8eb61787298dabd038`  
		Last Modified: Tue, 12 May 2026 21:46:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be3876fb1fb1aa225ec51618fb8695125ab068d1330b824dd42f3dc53189af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d955a6fc3dc02d59c9fb42d9f33e9495a86d8f79d66bc63047161935f99679`

```dockerfile
```

-	Layers:
	-	`sha256:5eaaae02daa457bdde2cedc9c58194d6fcea3e4638aa4bc67fdf84f0e20a0be3`  
		Last Modified: Tue, 12 May 2026 21:46:17 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:385d1f1c952154cdf0ee9a6533f91c0ffed8cf8ef5a40210fbaa998652b49f35`  
		Last Modified: Tue, 12 May 2026 21:46:16 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bb84a9490304cfd0d63a15de7a1c8c163872c4fff618a1daa9b226470bb846c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfd5b6c1381551d158f6910246a52947247413d9ed67323e514ba04c2aeda2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:45:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:45:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:45:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d830060a6374abe95fd009d9d23cdb8c0f764560deb428a51b472970047b1a6b`  
		Last Modified: Tue, 12 May 2026 21:45:36 GMT  
		Size: 54.3 MB (54272926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3fa45c5a11fbc838f8f85f9e6db670b302e8ab1c3d2cf578210dcb9e51231d`  
		Last Modified: Tue, 12 May 2026 21:46:17 GMT  
		Size: 81.2 MB (81174294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f2c78e80d2fe17dfab691548a163853ad026dbe92c317f6731129d05860dcf`  
		Last Modified: Tue, 12 May 2026 21:46:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:64bab6b8c58d6d2c967cd37f7e9f8a0617e9e8f2c40c962d77900b3584621635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf1ab220f7e45c97a77d8fb3996453998c5c83137e23d39d73dcbbe5e2726db`

```dockerfile
```

-	Layers:
	-	`sha256:13cd666828580c95c58e281afc5a94055e265ca743d6a3a22abe83311f4abf96`  
		Last Modified: Tue, 12 May 2026 21:46:15 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30af2c6a5602c466bb36b78a0cad17a6a74a4dad3ae880a5eac6d9a8ad25cb5a`  
		Last Modified: Tue, 12 May 2026 21:46:14 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5647e40ac992d7269a47b999dcb85dc24f06f5f05b9e3c0a3ae1c82fa7a54519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc3ce66503e19c7a9ff6999f9e65b1b6d68522754923da47f6a8ca4e4b1af8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:51:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:51:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:51:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa7d740aa4a391a491e87b17a4fe3345cda52e4cc8e4643ef6ba862a8c0d8c`  
		Last Modified: Tue, 12 May 2026 21:51:52 GMT  
		Size: 87.0 MB (87004213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f15b211cc2d16a9ae7487846c3a2511cd7c3a3e248cce33e2cc3ffe7eb6166`  
		Last Modified: Tue, 12 May 2026 21:51:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:987af2fe1854dfa7323bfd33271aeabd7ae82af38e664704ad10c9735edeeffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd17724837a9e3de681edef795f9a5a9949526c94bf1409df685873af64084`

```dockerfile
```

-	Layers:
	-	`sha256:09d60a8d002216f0f251807c5f9dcc4de8513a23319e8b7407b2e60e49942e42`  
		Last Modified: Tue, 12 May 2026 21:51:50 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57ce405b1c38dd28ac1446b238f5683938e18cf1b9fb898267bc2662d4b208f`  
		Last Modified: Tue, 12 May 2026 21:51:49 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
