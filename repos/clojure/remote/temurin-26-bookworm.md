## `clojure:temurin-26-bookworm`

```console
$ docker pull clojure@sha256:75d38c4a62fbe404df50d213bb6b023555ff221deb6c8ec2721f9eb29ccfcfd7
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

### `clojure:temurin-26-bookworm` - linux; amd64

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

### `clojure:temurin-26-bookworm` - unknown; unknown

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

### `clojure:temurin-26-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b84483c3d765707237fd118bd18f7469b4910775fb2426897cfab043704eb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222941416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ccdbbf3ed4f19a4f3eec283c7ff773c9716bb208830f7ee17241d7774d5a7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:19:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:19:33 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:19:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:19:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab378b237c2cefccf5bdda171268e7c5e062ce5efe14808e59b38410c8ae6b17`  
		Last Modified: Wed, 15 Apr 2026 22:20:11 GMT  
		Size: 93.4 MB (93395214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeef3355232728deb18223896e008eb4f28a93b27bbf0ddbdf02515519c9c57`  
		Last Modified: Wed, 15 Apr 2026 22:20:11 GMT  
		Size: 81.2 MB (81171899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfaa0889babeebd3bc79ed4672ef5dd6ab9294e96c9b7321bec17629043416a`  
		Last Modified: Wed, 15 Apr 2026 22:20:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67344a64de6a7248c5a012b9b270ce3ac22904ecd5049db13ddc9fd3d09a8847`  
		Last Modified: Wed, 15 Apr 2026 22:20:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc3023a6fce53a85b32165382889bf18a01d9ec4af04ac2ef49a3813a6f73431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0382cc6c8f6ed37f3bebe272de3f0eb010dd480f722636f8a3292f52fc6868`

```dockerfile
```

-	Layers:
	-	`sha256:89a6f11e23fefad91fb6334dc0865db12080648aeb29c62f9ab0fbaa743d0d50`  
		Last Modified: Wed, 15 Apr 2026 22:20:08 GMT  
		Size: 7.4 MB (7350274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8118b2eb5a42d7e5fddcab91d3ba64ecb115dccc660d2cbc28aa3cf2cc35de25`  
		Last Modified: Wed, 15 Apr 2026 22:20:08 GMT  
		Size: 16.6 KB (16597 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:4a9ce04e37617329c2b64dd562cc2f295687198d4f1172842f4b8fe726713c2c
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

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:63f9512fcbc7162bad635b41bff289dd26ea602d7d179eab48a56595cecad686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cb9b848f1ebc4860cddce5f91ddec3a5e44790eaa94fe998d294185cef81e6`

```dockerfile
```

-	Layers:
	-	`sha256:028560077e9643b18032ee075f0512672020deb5ecf2c6bb90ca70ceb3b8de5f`  
		Last Modified: Thu, 16 Apr 2026 03:17:03 GMT  
		Size: 7.3 MB (7333654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0eedcf349d2b3870b492fa8b7230f93da2a7099dc8eb83db9c4b774645c2ff`  
		Last Modified: Thu, 16 Apr 2026 03:17:02 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e4014008d168d526f699e2b4989bace929f789b2b4769acbabe5ced384417a50
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

### `clojure:temurin-26-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:99bc63e6209225314e075630ba3fd132071bb68847569552099e709f939182d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c50a9fa44b724a9441b415f615fd041e72b9a5ed0c4568a4d18840b8ea9989`

```dockerfile
```

-	Layers:
	-	`sha256:4085187a567935d84142ee5107ebb6d1d34deeb47a826dd1696fa7f10b52b7ed`  
		Last Modified: Thu, 16 Apr 2026 00:47:05 GMT  
		Size: 7.3 MB (7320995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cb105eb95d902c0f72e5da5f66fd3b00d61c2a37b35d22fdf1ed7712761d0e`  
		Last Modified: Thu, 16 Apr 2026 00:47:05 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
