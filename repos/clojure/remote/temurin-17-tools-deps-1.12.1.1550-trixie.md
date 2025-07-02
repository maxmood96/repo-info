## `clojure:temurin-17-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:ef07a0af281b47be3cd93cb83f32f8ad97798f23a7d7758246a495da0a6a109c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:684140f8d41722bea7cd565b923e1c24a7d6d455417c2e1386947c906612cd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279254966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214d981386f754161074d08bd4b2ad9ef779609fb2971c9ded3117beb6a7b01f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6730b76d5af51ccc3b319bcab87ceb24db7f72f319da6e8bc117cbd017d79b3c`  
		Last Modified: Wed, 02 Jul 2025 09:52:01 GMT  
		Size: 144.6 MB (144635065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11928356ca6654a55e2221b2d1031c26e478bce83cb2ddde82a1135a687de0a4`  
		Last Modified: Wed, 02 Jul 2025 04:17:37 GMT  
		Size: 85.4 MB (85354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0020f651b94be401155c14f5dd5da59311c391cabf5e5b59517e3895e483b4`  
		Last Modified: Wed, 02 Jul 2025 04:17:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcd7529ab186f1cd5f1b2f4e2036ad5de46e8c67c19c9adc4aa0384e772e07c`  
		Last Modified: Wed, 02 Jul 2025 04:17:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:879284e29ea3d2d13c8d8aded9f95834e9e8037392b444a447cd9f31f8ced04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c726674346a72ea52d99541faa4f321bfb0d5ff15f04b7981f41494de29bcc78`

```dockerfile
```

-	Layers:
	-	`sha256:4373796a30ee1afeaa0a91826359730b6a051b33ea38cec33c860fef5bf3a7a6`  
		Last Modified: Wed, 02 Jul 2025 06:38:45 GMT  
		Size: 7.5 MB (7459153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d762705ed242442dbbdd811b101692ecd8cbd678cb772faf24ee46b58c3205d`  
		Last Modified: Wed, 02 Jul 2025 06:38:46 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:723652a193c2997b587922a83b0e379e3c555320ab8f9f6cfd758fe3355a6e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278315726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a2987e7448c5c96364d803659eb978311f346c456932baa91de858feeae44f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3cbfc8496425cff417dbe510b3ca510428c76cf99902087277dfb0427ebd3d`  
		Last Modified: Wed, 02 Jul 2025 16:31:06 GMT  
		Size: 143.5 MB (143512654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973baf5bcbfeb5100b24566676ca0d2b49f9f5589298caccc3b812ee729f0476`  
		Last Modified: Wed, 02 Jul 2025 12:40:33 GMT  
		Size: 85.2 MB (85171878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4319eaaac95a2e5388f85fc5c401d19711196d6cb2e73904ab67a06e98fcf1`  
		Last Modified: Wed, 02 Jul 2025 12:40:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76bf29e492690a8676db340697b2cbf71c7299ef5fbe4cc800e49818432c93`  
		Last Modified: Wed, 02 Jul 2025 12:40:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:190fd4b1eb926dac9a64597bfda0b7216618e51c252e06ab9dea8975eac3ad37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d6f649663bed67c7c2171cfb048aded07f4b19c5035d8972d9402cbb0b836a`

```dockerfile
```

-	Layers:
	-	`sha256:3215f3f9d3bb7f271213c5a757be07690614cc9a90ba9e54aeb29ef3ec127c58`  
		Last Modified: Wed, 02 Jul 2025 15:39:03 GMT  
		Size: 7.5 MB (7466183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f5b6d1216b9985862d743f2ba916b8e2c5bc776b4c660b02c39aa8b9670f0f`  
		Last Modified: Wed, 02 Jul 2025 15:39:04 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6ad62a5ea1e3bc2b738c65af40391fbe6fd40218eb68ad2e8f0e7035cb6c4e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288148027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d45efe22d7c28db8596198ce7f6275bdf5138b547cda308febbd2bb078f4a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621c1ba1ddac796407b592f4701d2764372a507ce67dbef534e5e6b3aaf2745d`  
		Last Modified: Wed, 02 Jul 2025 10:32:49 GMT  
		Size: 144.3 MB (144280303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a1a7ae31e846fbc20b7d0bad2c1862f7945e2f2bfbdddc0cdb443a019dcd0`  
		Last Modified: Wed, 02 Jul 2025 10:41:26 GMT  
		Size: 90.8 MB (90769445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4633f41c8dddd73382648163c1b82a15b36194809f78f9198d1c3d8938996b95`  
		Last Modified: Wed, 02 Jul 2025 10:41:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261252cd092c246036b8da11c47dab7bb9e48c4fd70a57eb2b13a5ce2bda2e19`  
		Last Modified: Wed, 02 Jul 2025 10:41:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7ef91d0708efa9e1bbecd6f1e208394ed38edbd317d5e7f1a7a86ca15e7ecc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b960210c037a272efd1ba7254dee68b0aba062c37f9ee2e444fe23b5992a9fb`

```dockerfile
```

-	Layers:
	-	`sha256:39220ebc6a843ae6b8c1d32e3bf913bfbdedd8fa37522d9623198ff546e5767c`  
		Last Modified: Wed, 02 Jul 2025 12:38:25 GMT  
		Size: 7.5 MB (7463570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9281f901fc1242a18a899b68e73fcb730b41bd8798c7c6c1a4b5585ae39310`  
		Last Modified: Wed, 02 Jul 2025 12:38:25 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:1332c7e525390577cfebf351a0bfff417b2e81e0c3c7a3df10e6fd8d71617fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bf84adc60e683b206a5912c5889c9bc84583e3f25a02bd7eb9c594dc4b5832`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925a9db3ce42da0b155823eec851a05ae02685ee999a7b27b951a14d544d2a0`  
		Last Modified: Wed, 02 Jul 2025 13:38:24 GMT  
		Size: 138.5 MB (138492446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c0e6577256977b531e8c6c5e3de7970e01d81399c2fd1a914c80a5a3b0606`  
		Last Modified: Wed, 02 Jul 2025 08:49:03 GMT  
		Size: 84.2 MB (84238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e535be174d5ee868fa807a88ae420716a75c94615102181044d9aeaf61237aaf`  
		Last Modified: Wed, 02 Jul 2025 08:48:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39174747103ba3ac2b972b1ff032f26987689b8184f998d0aed03ab8865833`  
		Last Modified: Wed, 02 Jul 2025 08:48:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:86d6e5ef55b61a5b566378b5f05e1c1e52bfb8dbb14550aa07f0637b1825461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8746a48ed2ef026afc946e9663d9cffe2e6740e2a285b25be10d0cb8a6a81132`

```dockerfile
```

-	Layers:
	-	`sha256:3dabe69d5983cc0223a90f3f9a05fdcd74efa6d80217e475aae1b85205cc3965`  
		Last Modified: Wed, 02 Jul 2025 09:38:25 GMT  
		Size: 7.4 MB (7445145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5410e124fa0a323220f492af83868d4fd8c97f09454b5845e06c81fb8eb157`  
		Last Modified: Wed, 02 Jul 2025 09:38:26 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:57ab76d41019fc046d12996ba7f3b3ed2add5a6cddc9533adf696cd81872a2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270352948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90658f21adfa55821e6334d4edcb9c9d919a3b9a4250952cc5565879598f06d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d753f0bcdf961e8d01c564825d10e4f89ae0454c2ba51061240967e85cbdf`  
		Last Modified: Wed, 02 Jul 2025 13:38:36 GMT  
		Size: 134.7 MB (134673602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206035f6da52a6bc4ae077cd8e737db0810bf66a08b66e225e05e984102f6b6c`  
		Last Modified: Wed, 02 Jul 2025 06:43:32 GMT  
		Size: 86.3 MB (86334647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea72ace5e3044cf2f3b4327301bb7e84cfc9d3638b7ac197be8d1222fd71af`  
		Last Modified: Wed, 02 Jul 2025 06:43:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017012b2961e8620609aeeb33d649d0b7118658c9e1876a4ed8fe955934fc6d3`  
		Last Modified: Wed, 02 Jul 2025 06:43:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ded5b8d8b5b07b1883d657780b5b337a8df3453b4d2a1561aa809077139bd9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e685649b0bc27530e330a1aae1d12496146e181150e94c46143db58d061d28b3`

```dockerfile
```

-	Layers:
	-	`sha256:ec9e28ba2181a46a3a007cc871b63f95ee393c78acf5d6d563334b76157f8752`  
		Last Modified: Wed, 02 Jul 2025 09:38:31 GMT  
		Size: 7.5 MB (7455075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d0a4da1fa191fea89db2dc3320dafee665049001f3f393cb84d6c570c1784d`  
		Last Modified: Wed, 02 Jul 2025 09:38:32 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
