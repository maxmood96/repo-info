## `clojure:temurin-26-tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:978966e70228976835f84121c52bedc903f6a741884b2127000ea44f108ccc07
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

### `clojure:temurin-26-tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:bd64109975b8f22888d3462b8ea16cbea2c2f4ccb22ba2ec688c3dac58543f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224114008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1d1ba309eeb4495000679f79370e29e2ac58ba4f3be61b41039cbba19733d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:07:46 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04d692e549b293195f34614ab60796217236af000e92e84964275d201ea9f9`  
		Last Modified: Wed, 15 Apr 2026 22:08:22 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce85d10e9b438d2feb2b67e1cd6d730581c75cf69a11e6abf6d9f12207d4e1`  
		Last Modified: Wed, 15 Apr 2026 22:08:22 GMT  
		Size: 81.2 MB (81168453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655ab1ee71cbe82494d0d6b1481dd46ec559adaf5da986ea8d7258c788503025`  
		Last Modified: Wed, 15 Apr 2026 22:08:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71a7f573719c6e1398b65efb328bd367ceb2dcf5d322237382e117bbb2a3235`  
		Last Modified: Wed, 15 Apr 2026 22:08:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:39bc6e137135f0c720182e021ff5b8932a5bfaddf22e55570bf634c09ba5a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1d393fdd5d40f4447f0db6b1bb9b314e509e6bd510ea23c194b32d3044027c`

```dockerfile
```

-	Layers:
	-	`sha256:68be0b832864505b19a572b09dee6e44f4f31f09f2e04a218c31807132616d10`  
		Last Modified: Wed, 15 Apr 2026 22:08:18 GMT  
		Size: 7.3 MB (7344490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf8c6411534cba6f34f3ce9b2b5db16b867956df982cdee1fd02de1d775f2d5`  
		Last Modified: Wed, 15 Apr 2026 22:08:18 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:763c627073adcc8a99cc3ed59a47cc3f8b2d2fa6aad2a63c86561b2dd51f363a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222943470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b3495e401a8d5116101854ca6ba962f377141140179da37c77bce1e9b870f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:37:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:00 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe459180190a61971a3ed554740a7405fb0ad28deff6b598c1672077a36b432`  
		Last Modified: Thu, 09 Apr 2026 23:37:38 GMT  
		Size: 93.4 MB (93395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9269f89400f58ba9f27428797aa184047f7f911e7e4e8a78ad1e32d0d2e8b`  
		Last Modified: Thu, 09 Apr 2026 23:37:38 GMT  
		Size: 81.2 MB (81173965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4973098ca5e8926bb75b8a04b3a482c0ca11efd855d43e93657eee70c22a8842`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6b501c53208652623aa0c2bd525ad2c3fefeea2bd486d1971265ab7d0113e6`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:f9965e97936f4cca18a3e9173e186bf49dcc15217832f35369573bf94d96e2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b7440959ab7b32a0a94cdf19bb94b4dd0442bfe3292b1427a4e9585b634a1`

```dockerfile
```

-	Layers:
	-	`sha256:b760f000e1fcefeb3463b5f39c464dd54b8124e00859a79e2dc4f77785fd8db2`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 7.4 MB (7350274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318c99f2234b963f8f3076aeef741f3b44b0206413e6bdd9b2d72457a158ff9b`  
		Last Modified: Thu, 09 Apr 2026 23:37:34 GMT  
		Size: 16.6 KB (16597 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:f8defcc2478dba0b4b0a88dfdad9e645a206bb81bbdee6ee323427c8ddd19171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233123727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b904029ce4dfbba361ed22260def671de07f86ed7fdfe6353d47ddd74c9b2da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:49:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:49:05 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:55:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:55:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:55:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:55:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bb937b64e28b9440675ccbc228210a99b8d8484e299953df825953180b5f5`  
		Last Modified: Fri, 10 Apr 2026 00:50:20 GMT  
		Size: 93.8 MB (93781433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e06babe786768a3af7a08ac0e27c2469d113f91699dbc54d7741bebe5a79673`  
		Last Modified: Fri, 10 Apr 2026 00:56:00 GMT  
		Size: 87.0 MB (87004316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5a1566efa6e60946982469ea2eb76c5b58c21a14f7e95b23a5616cfcc9b2c`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c9fee73bbbbcb7161f58ca4ec903f171cba7e44036a6b3de4ef9215ce50c7a`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:e38fcd19768b68785bd6c68ac8b7b0903a48af1fabe84838b894b6ff13a5c1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41ae4de92b9f1087b6d3d0fb36798194139c8920f324cc727905be0224f46bc`

```dockerfile
```

-	Layers:
	-	`sha256:05783f37aee0ec4bd8d708c55b62e43476d4a37790e536d6d1b6f6b18f6a0ff2`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 7.3 MB (7333654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c489bdb2c382cb70c59f5e765bc6dc641ab8e519b74aee57591ea95d72ad2162`  
		Last Modified: Fri, 10 Apr 2026 00:55:58 GMT  
		Size: 16.5 KB (16514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:930eaa024ca59ff49e4ab97bc77b44c44b32b1dda060f437af69b1fd26e0c09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217676677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d9e9a04dee0f685a14ba9eedda33b6d566f03f144131c7abadd80f957c7e38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:43:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:43:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:43:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:43:20 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:44:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:44:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:44:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4374cefdbacee456d8ed008c1f311f90f13f2b652def32ee01d354d19f349fd7`  
		Last Modified: Thu, 09 Apr 2026 23:44:03 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981499af759fb6d244f56ea5e147e3b2e3e15371b11dee2bd300ce537ad52cb`  
		Last Modified: Thu, 09 Apr 2026 23:45:10 GMT  
		Size: 80.0 MB (79979806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9cfdff2b0b84521d4b4545bbe101ebe383c71f1c2c08c7e563de371fd995d7`  
		Last Modified: Thu, 09 Apr 2026 23:45:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dac0378a9a0ea19e94977f155843cb1157dbb1f887c6fd4332e0f9cce3687db`  
		Last Modified: Thu, 09 Apr 2026 23:45:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:c8bcb512556a73e49a28890eed3752a927c7e3c28411a2f4a953fce604eaa69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8387c64921f99b570183d16b8784b71a9f509c3135f7ca05078aba863620c9c`

```dockerfile
```

-	Layers:
	-	`sha256:ec1581b3a2dbfa446dee0fa80f4daccbf04087aef7fb65c039aff2604e916909`  
		Last Modified: Thu, 09 Apr 2026 23:45:09 GMT  
		Size: 7.3 MB (7320995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b10bd950b2ab455df3ceda364e4312fa163b338633364bcf47a43efff36e10`  
		Last Modified: Thu, 09 Apr 2026 23:45:08 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
