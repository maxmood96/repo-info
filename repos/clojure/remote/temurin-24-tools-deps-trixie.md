## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:7ee3b0b3cd4024569c5e38e6dbd0f3cc7c55459ce83209f527202a9f78efd385
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

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:909bf44ff8537c32c74c23f6cc3f0ebaa8ba7186acef6519891b29535ca91b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224572306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36057768c6a68e489f5d16b260aa0ef1b857898dfde5b30ef137b637f3b90a6f`
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
	-	`sha256:6a8609c9c73f9c388dc1a614c2ece6016f03c02073c3f53602b9ca4bc4cb7741`  
		Last Modified: Wed, 02 Jul 2025 04:17:44 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872adf2c5a575010734881521f0311dd569c6458d592b05994e5e0370f32d43`  
		Last Modified: Wed, 02 Jul 2025 04:17:46 GMT  
		Size: 85.4 MB (85355390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70a8c662d84105f0b8357a59826368fb22517f968d863ab4b122e76341df40`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b833070a83bbe781f33742ff1b46afab7621e9c728b2a13c59614927233351`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d03899f81061e2e434b0bb5c7b0b7e9f5c2135278170a7b1a821f55342566e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9130ae3f28c53070cce4d101daaffaabb68a52dcf88e85be6982557cffb10b43`

```dockerfile
```

-	Layers:
	-	`sha256:5efb9f77c676ace09869c4c909942c702a44cffcb84b26fe537912904258161e`  
		Last Modified: Wed, 02 Jul 2025 06:42:24 GMT  
		Size: 7.4 MB (7409799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59781be4f76544be1099c0309b80933d7f60cc2245d28f679eba1601800e261e`  
		Last Modified: Wed, 02 Jul 2025 06:42:24 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06b2c82195c7bc60c2b7dafdc599960a3d4e46da179095d764e249c49e0d1f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223894294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3474a1b0eff570505a8fca6bdf165200bce1bbb61d690e0e49028e22bc0997b1`
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
	-	`sha256:4a9db87f3989ea7436daef5edd944544f5c2375c33cbbe49a462cd992ba6cde4`  
		Last Modified: Tue, 01 Jul 2025 12:41:14 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ff17d976a08aaec3b0924c4206b08b8e0732b6d827b0867f81423f2a9a1e5`  
		Last Modified: Tue, 01 Jul 2025 12:45:02 GMT  
		Size: 85.2 MB (85171826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5677609e06cff49ebfb40162dd961757df8cb6e7ff0c6b29cf6f0fe10832c6`  
		Last Modified: Tue, 01 Jul 2025 12:44:56 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de20b743604eb8b4e38ff4654f74cf0aa46ef8ca4244491dc69131fcc21b718`  
		Last Modified: Tue, 01 Jul 2025 12:44:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb3b4a9b89e467c3085fe3d765d7fdd5f865840e7e09550217d1966543ffaf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89e2f69258c2ba5c9ebc3a736d4e0faa2f5e12ecad49e77256c03b650ea5739`

```dockerfile
```

-	Layers:
	-	`sha256:75a8c9ac43ab153e4564553c9a27dd84833baf5c03ac13b13ac731b0a4307ac3`  
		Last Modified: Tue, 01 Jul 2025 15:41:09 GMT  
		Size: 7.4 MB (7416826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46f196536454ce47e952015156e532e90e884d579ff1b9e6f8b3f32327dc60e`  
		Last Modified: Tue, 01 Jul 2025 15:41:10 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:de21a1c8f2d10e6860ed2e3d72b1b9d2efeaf1cdebd8c2ed7320bd26546c0fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233789248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf0631313b2266be024ecb65b32a3cb44969aa2b38fb781f339788069ef93d7`
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
	-	`sha256:023db990e340f457ab72bf2cfaeeb935b2a5d1eb6d982f2305d773aa3de17226`  
		Last Modified: Tue, 01 Jul 2025 13:21:30 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab0b52189bafcadcca120efb4f2c6660a5b0218bf833d78c0b995b306f4dc8f`  
		Last Modified: Tue, 01 Jul 2025 09:20:24 GMT  
		Size: 90.8 MB (90770694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e58cff2cb72256ef4bc5ad9457a6afd1f39a60e2e701b2d45e8bd26c8b2262`  
		Last Modified: Tue, 01 Jul 2025 09:20:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641eb09db0289ad382b5bab822d53bb1d1209ff8bea2d06b71843edc1d9b55e7`  
		Last Modified: Tue, 01 Jul 2025 09:20:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e672131dc65d54fa040f0d2166cd2aaca1f866d7c4117fd4ecee1dc16d4ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1134b4b59de0f61a3236f5f25b286f48d61528ecc591c4aaac54c82d39092c44`

```dockerfile
```

-	Layers:
	-	`sha256:111591f875cc2bec841252dac1ce7e0443cca0d3687fe8ddf611430862db752f`  
		Last Modified: Tue, 01 Jul 2025 12:38:21 GMT  
		Size: 7.4 MB (7415514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994d0e3dd9c77d6a0f5e5f61b71925044bf13a41836878ca8a2370c04172a6c5`  
		Last Modified: Tue, 01 Jul 2025 12:38:22 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d0efb92ea381b5f7bd58e0ebed10d4efd215aa2122ccc82c7c05dfed217896aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219611590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892e4b809bcec4629547fea088bfe7daa3fb76aaa292b3ea27a56e10ac553bb8`
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
	-	`sha256:f120b17727d388dbdc6b555b4871b73604f60d8e50666c67171b05dec72894dd`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3465929612b1cde352b1dad40f146bcb209704e28a8e5a15548e47be7e2ed7f`  
		Last Modified: Tue, 01 Jul 2025 13:33:29 GMT  
		Size: 84.2 MB (84238227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5cad5cab33ea075270de60c0f480c42b650bb5c9fb772d4bf7b0f6d44815b0`  
		Last Modified: Tue, 01 Jul 2025 03:45:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9eb1478c1d35417f4fbf51951ef6418fe6a55be43698389640c345cfef9c13`  
		Last Modified: Tue, 01 Jul 2025 03:45:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c876f58b6e5ade7eec1e55753a037ee988a5501e22fca6625f4dfee5e61870ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c1ab7e76531618d841e50c10a8eabc2c713da2e0474a14995b8ae7fe1998`

```dockerfile
```

-	Layers:
	-	`sha256:085d549d8c4469bca11ae21a7bfa7a80e53aab0d8f4228d0db8d92a06909ceef`  
		Last Modified: Tue, 01 Jul 2025 06:42:06 GMT  
		Size: 7.4 MB (7397707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab398b2a46fd5fa2b10334f865778c90d323dce7e0b0bd57a0771e6749b32ec`  
		Last Modified: Tue, 01 Jul 2025 06:42:07 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5c70d02b86d7f604c16daf3adf3ca18193e1b1c3c4e546fa5c043b5d1f3833ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220896274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0f4456dc4221dff0395d16bbd5c9095905d37bdb86ad08f1be53317b885cb`
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
	-	`sha256:3cc4f9cbbad9b79641e4f5ac67263deac9aa43001430d2662bc7db69f2fcfe7a`  
		Last Modified: Wed, 02 Jul 2025 06:58:54 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7422fc92008076eda4c671d9d3941fa635dada969726d35f2b77a9fa9a3cb1ee`  
		Last Modified: Wed, 02 Jul 2025 07:04:25 GMT  
		Size: 86.3 MB (86334770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707e8a8767b03df22ed062c276194f5ed587ebd1d2e1854fa48b67fa36125d79`  
		Last Modified: Wed, 02 Jul 2025 07:04:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d6ca7601fc34253b635d879d4c11e58480ec9042cea534c6dd4f428d15b9ee`  
		Last Modified: Wed, 02 Jul 2025 07:04:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:68b8ea51bede30ae2831fab1fd3c6d7ddb1af8e0f8c8aebc3df6001d6c11a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7860ee9c0a1611613a2bbb674d951d8e9e8033770b84088ce7853eb29012c`

```dockerfile
```

-	Layers:
	-	`sha256:4a0ea51fcb6c8ceef2fbfa2dda62108dcba47847db8e9b470dff45c00753fb90`  
		Last Modified: Wed, 02 Jul 2025 09:41:44 GMT  
		Size: 7.4 MB (7408269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040e436fafa6a1b8561e0a304c375cef2f14a16bbed0c30da881f283f92e8887`  
		Last Modified: Wed, 02 Jul 2025 09:41:45 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
