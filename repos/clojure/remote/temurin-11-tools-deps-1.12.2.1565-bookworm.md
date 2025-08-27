## `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:e83a37b91ae37f4a191f1b3e23678426905c5025047778ae4db28bde738892e0
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

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f062d8565ab5377a4e05d8d7466488c02512aac3a2224e3f556c6f6204621e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275291685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58339df19d3d146fd296c1507667900f3e5be921e3cb4dcc398c36e0624212`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6c46451a48058ee746452644261c795637d96c04365d1fe6cb7f498e9133e3`  
		Last Modified: Tue, 26 Aug 2025 23:01:54 GMT  
		Size: 145.7 MB (145658173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0793b88f71613a5cedc2f51981e9df2fbfcf1e306cdf1b80a200faacdefbba1`  
		Last Modified: Tue, 26 Aug 2025 17:27:59 GMT  
		Size: 81.1 MB (81138354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57444a4f0cc82dccf11e8085fedc6942eb6dada3699800e5d1df19ba9f3103ba`  
		Last Modified: Tue, 26 Aug 2025 17:27:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:33a6a595e5fa3a71a8569ff6a166e7a17c8af1a13631a67eed1e02c54261495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32dcd03b7fcc8700739ca09caea0530e03b756c206624fe3b69be00c56db224`

```dockerfile
```

-	Layers:
	-	`sha256:9cf63c35be0480673faeeab600a65af21cfb7f4a3ad65b0b2f9ce577564d631f`  
		Last Modified: Tue, 26 Aug 2025 18:35:04 GMT  
		Size: 7.4 MB (7388438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dd44494ea48a7a4c838194040dd77305112b827c0a612389ac5553a15a8dfe`  
		Last Modified: Tue, 26 Aug 2025 18:35:05 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d24708ba48899b9558fc9b547c69c015cbef594f94ea2e5a0b81149fb554cfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271813042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c593314058e846d4d7a641920243c3e1fd0ec01affecae11f20af08e6ec08fcb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e393506147fbd7055e29d89728a0fc86ede72088d0c45d92332a69b6e1676`  
		Last Modified: Tue, 19 Aug 2025 04:20:50 GMT  
		Size: 142.5 MB (142460572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddec2d8475df0bda3c4e076dbdad69eba91387c4533e12f2edba7c633a13ca1`  
		Last Modified: Tue, 26 Aug 2025 17:35:26 GMT  
		Size: 81.0 MB (81009373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3443ee9d7fea7e39c5fb095e7ff980efa5e33db9a36d108c37b9b551e801a4`  
		Last Modified: Tue, 26 Aug 2025 17:35:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:267142f0b55d5dea989220a64d589a7f34e97a0e86d75c446c33d6534b0e4ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0423ee511af4fde177337c75871a21620193e67fadf23549603a18895b27ad9`

```dockerfile
```

-	Layers:
	-	`sha256:f539f705ddf3f374003d7f0b3693adfba62521762d286657dd6d6b4ae55d23df`  
		Last Modified: Tue, 26 Aug 2025 18:35:11 GMT  
		Size: 7.4 MB (7394819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb903832da9c0db05bc03a28bb20e9c111bfb4eb3989328338e69ec253064088`  
		Last Modified: Tue, 26 Aug 2025 18:35:12 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:102aff611e3d1d97d7694083f94aa21de4bbfa9416476957e6dab83dcec4d33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272164585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e9551b5fee88b093f4d6e9fb4b85a1861319752a3cf91f24f9fea4d6e8f6fd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cbc261facd2ea551ba4f1d307ad561b88de934025d4d92da0a46a7a5d5385`  
		Last Modified: Sun, 24 Aug 2025 07:13:30 GMT  
		Size: 132.9 MB (132853318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993bdb2865ec883ece8a2f28d83d97bc8ea76ca5a6f4358e1e144f6130721bfc`  
		Last Modified: Tue, 26 Aug 2025 23:08:56 GMT  
		Size: 87.0 MB (86972544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3c5b71fbb62ac1e64316a2848335d1383a0d151ab5ff6b31a53b04b8a72fe`  
		Last Modified: Tue, 26 Aug 2025 17:45:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:93496c7cd70388de4a822f73e55c8439c539e7f308c2675fb928bb9077e8c158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ca8a374b0cbf5613c11ad66a211326b8d1e4ec5c93bcc5bb3a6c4da03f4658`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b992f4e92427d032a4770def843d6933c28a9367f774c94723d123796411a`  
		Last Modified: Tue, 26 Aug 2025 18:35:20 GMT  
		Size: 7.4 MB (7393027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000360117a8cb6d6e61410db46fb52c6ceae4006cdd8f7d8f2b6425686e92e77`  
		Last Modified: Tue, 26 Aug 2025 18:35:21 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:81a88a302dd27eb829bd503dfc74d49da7b8227c7546176d1617bd7db49b32b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252726308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463baa6554d51a8c91d5b02d255d35c5b4ef32f7cd3f59bacb0af21375cd19f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7efb0bde79f746db6b5bf0ea02c772ab6b0f4c21efe10e39411b960291cabf`  
		Last Modified: Mon, 18 Aug 2025 17:03:28 GMT  
		Size: 125.6 MB (125622103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385771434e5af4d1671466a9b3ebde76aa300709355f1fc9e4436689458cd3b`  
		Last Modified: Tue, 26 Aug 2025 18:55:28 GMT  
		Size: 80.0 MB (79953693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35572daefa77bf081ab02ce198abc2d765839cc633fb6e981705f7de89386b85`  
		Last Modified: Tue, 26 Aug 2025 18:55:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:600c121803fed3d89f29b45253045a60c523031d0c7b954644f046780026c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18ccbce7e6c8d30dba99b75bf3f78da513b50d7d069b2ab5f3ffcbcd8932073`

```dockerfile
```

-	Layers:
	-	`sha256:42e4e52b334cba8b886fe4fefcfb49c90870c176eab695f9db6a0f05eebd672f`  
		Last Modified: Tue, 26 Aug 2025 21:34:50 GMT  
		Size: 7.4 MB (7379761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c986f71bdd2d16d4aded2e9e1c5abaed299e679e48685721f9946679e69b63fb`  
		Last Modified: Tue, 26 Aug 2025 21:34:51 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
