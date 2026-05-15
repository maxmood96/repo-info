## `clojure:temurin-17-tools-deps-1.12.5.1638-trixie`

```console
$ docker pull clojure@sha256:69c14941dd4ffc2477eaa30e284a7bea5d5b5c2862314c027baa6af16f30c329
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

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8495da01acd0b7e4aa28d20972d751c99e67e1f27d32b2c063f7c28adda2a87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280812614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39954d454e929f20063e899b93788d9d49afcb3d26ca4071256434639bf08a59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:16 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:16 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afb1940e1bdde2fa1c0cfafc70f2e1d77a92d0aab7141eeb66a33a917760c3d`  
		Last Modified: Thu, 14 May 2026 23:35:53 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374707a0cb5d279028779101e9c6c9c4bbb1f36986072b2d7918dce38e65535e`  
		Last Modified: Thu, 14 May 2026 23:35:55 GMT  
		Size: 85.6 MB (85603805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0383736926d15f8936aa1798f62b4d9c074a739c45952eb0479630b338abb73`  
		Last Modified: Thu, 14 May 2026 23:35:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa32f5f00db557499ab9700e28c332810c8b0d48830f41d76aa7ff71b3ebfecd`  
		Last Modified: Thu, 14 May 2026 23:35:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d1ba6d581d437c7029894faf291e2cc6b58c022adb163d9f7e67ac1c0412cbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe2d725191011afef07651b21a04c0cf0004932d0a9af732ad47f2f976f67f3`

```dockerfile
```

-	Layers:
	-	`sha256:4f197faacadb1c73f2b92ad8697344e550d14cf944964fab37e26d3b275e6aa8`  
		Last Modified: Thu, 14 May 2026 23:35:52 GMT  
		Size: 7.5 MB (7471382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580145e6345574f6255d9ac17cafca941ce755cc6e5a09c31c34ce1578ce8dff`  
		Last Modified: Thu, 14 May 2026 23:35:52 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1a656e6cccdada6f89b2efce613668f13b0649949f87f701d40e3c1a9920740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279809911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a044c5e3e573ce102e753844a78daa88044dfa116ae844125d57f04f602e04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:12 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:12 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf4806a6edcdceeb5a75e828c17ed9b0f0d3d9b1a7ba58e441b0842502feff`  
		Last Modified: Thu, 14 May 2026 23:35:56 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f0eec6d8a0c8c6c08485f573edefcea1e06680b61826ce577a56472f4682e`  
		Last Modified: Thu, 14 May 2026 23:35:54 GMT  
		Size: 85.4 MB (85415085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed025cad3628846e9355d714b2159abb2ea3abd23d61df8745640a9a5753dc`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea071b010937ef15e34bb631b2695b091e6346a17205b108da4055173509c5e4`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d742f9cd41d71c107c04711ab40ee6d604e5c4a554d7e7a712a938179533644c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98292acd37ac2fee4e9d2ec693bd49d4b718187e1d688ce0abb96e88a3840570`

```dockerfile
```

-	Layers:
	-	`sha256:a54c830e74577ef92654c3ed9a7f5222678931111ad851d4fcf3505923cf538f`  
		Last Modified: Thu, 14 May 2026 23:35:50 GMT  
		Size: 7.5 MB (7478412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9f147b8065cd448a644b40e2a72802c86d2f234344cd6b6a8c0a14a0af3fe5`  
		Last Modified: Thu, 14 May 2026 23:35:49 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b9be5b65f403312bccaf315c505cba0779a84a1b22379dc286b59097852c4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289898227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0024f2879e2faef620e3ebea2d1fad6489f72f86520aa493998f5a95eaa32e37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:31:41 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:45:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:45:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:45:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:45:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:45:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06742bfd6f3a4c91a065b055265b2edf944919541ee9c7934bc1931edc1dd4ae`  
		Last Modified: Sat, 09 May 2026 02:32:54 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68613044788bcfdf42bc7aa8dfccefc5d8917454e27d922dac819b5de36083`  
		Last Modified: Thu, 14 May 2026 23:46:14 GMT  
		Size: 91.0 MB (91007905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43ef93a9af866c96e6ebd008f38732f9cb9e6f80befe4310a7b2fea47276629`  
		Last Modified: Thu, 14 May 2026 23:46:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ef2bb0dd1ded28603861a441f9872d4626aff842c3019e30606b990b36b3a6`  
		Last Modified: Thu, 14 May 2026 23:46:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6a6846d468aac59dabaa9ad89d6af1aa7c73001342262d0a65208514d7973ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8fde0cab061e8aac6501a7c8e4981f53f949280e834044d2b722730a130db4`

```dockerfile
```

-	Layers:
	-	`sha256:24c3ec5d8c89fb25fa1ee9935f4ac9534be1300839cc23dbd7e0b7a9f5e0a8f4`  
		Last Modified: Thu, 14 May 2026 23:46:12 GMT  
		Size: 7.5 MB (7475803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00191ba628816a75396ac8e731eb07f58185f040ad816d641945ba2d02c63f6f`  
		Last Modified: Thu, 14 May 2026 23:46:12 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1233c7c25b00a4a505344b2a236abce50d27c4818523c99b4d0b9f3c8669c9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271850029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be07546645537797660eb14ee6eece3b92015668b4218e3e6371e80e31ac1b11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:51 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:51 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa8298eaf2592c145eb3df8dd181759e8c3d5b578a6fb605668478ef706f0f`  
		Last Modified: Thu, 14 May 2026 23:35:36 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1641cbd32edc69efc74cd27009286e3151271973cbb98f1a843ac649c49f60a3`  
		Last Modified: Thu, 14 May 2026 23:35:35 GMT  
		Size: 86.6 MB (86566273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8af8482ec564f84f98992740368421dc6bc5f3ede27cbb0257c3e951369ea`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dbf7176829702e2b81f3e38255c3d05a5cd1c1a09e3985988c44c371c376b6`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d910c54667d947fa00e8c0294726c8aabfcda1701990b0210b28eca7f4a4713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15471ea4af1b9252a1f948a28aa4aa46c9dbd2e0603d35fc3503337286a10427`

```dockerfile
```

-	Layers:
	-	`sha256:04a9d66029c01964d1b1d2211b4251c6cb194ee5ba3c81a842448a3dcd37cec5`  
		Last Modified: Thu, 14 May 2026 23:35:33 GMT  
		Size: 7.5 MB (7467304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6564d8e5e67f4cc70df9d1790368d5bfad188fcb9e5306597090ab11577d2c40`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
