## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:1d529bd6a862a599a57c1d97cbf8b968dd04c0f11506e0e4e693c0c70b30443d
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:06d12ab12d06a5d7c14a9b56f9f4a10af54e10edf023b80189801b6e03e59795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275296126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b3dd6c22a733971142af26bccea3925f74b783ac4e793a3c527887fd72993f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:46 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:01 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42170313e550e8d33ac304eb60e5a0b933c869d19982175a5d06ebcecf9cd707`  
		Last Modified: Mon, 09 Mar 2026 20:35:24 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7879460882eaf5ef7afe39b4897f7c38bb571629dc4919e5e4325f1f6f3790c5`  
		Last Modified: Mon, 09 Mar 2026 20:35:23 GMT  
		Size: 81.2 MB (81177594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54088d803437d680464d45749a3b38eba9601cbf047d7118e0d72f2278f1ffd1`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454cf845783cadb24f39f25890bc28a2cece4a294f56df4444a4c1598961df4e`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9c6e247366a66c8a4b3c310fd3b89de304b4c5fb9ed324d4d650f94cd9cf0dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6c6dea8d6492339a634d823a4e6c7ef8c689c694a82101be2c3e480f540ab9`

```dockerfile
```

-	Layers:
	-	`sha256:a61ef4bd2109f55395874708caaa9001c865f5ce5619aca319e0c18bec288f3c`  
		Last Modified: Mon, 09 Mar 2026 20:35:20 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2abcb58ba936896a6bc2bf8847663e677c7b8fa938c500df856d37a83dfde7`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f90a3ebceba7cb99105de954d9485fdacb3ea7ceab0843cf82c8e95a01972778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273968820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937f336616d864fb70559dda085c4b50ea158dd443ed9533be254d3a0f850fc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:44 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:00 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77817eebd3791be990528420151bb36579ce3b8a67a523913e00e31bca1cf7ad`  
		Last Modified: Mon, 09 Mar 2026 20:35:25 GMT  
		Size: 144.4 MB (144436184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c8291a789fd5cce4f1e9e78b4916ce69d4f442216b9e4fed6fbfdf8220f84`  
		Last Modified: Mon, 09 Mar 2026 20:35:23 GMT  
		Size: 81.2 MB (81158385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cb774747f5fd7cac1ec5c234e56ad74aef689b18faf85a6e23df194b6cee5`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f5ec61aa0d66c499c48a781b6d31e54357ab9ebe46fd4e312621a0e43ce1b2`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:206038da9c5654395a57d6343edf4670cfc06fcb80236638c40d90c502051972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfdbb062365992b74c147efacefa549ff321e9d75682a25740bc7d66ea7fd98`

```dockerfile
```

-	Layers:
	-	`sha256:a51bc8d199d3bb7a36a1e3207cb59cae5899a29e062a9a5c4d565fefc6d23420`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8894e8010a1c147e3701c4d5df36e299c42e5594134aa6043553e0740a82b34`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e3c5342562cdf6d5fe9eb2b4e0daa6acb4eb637554f50cdbf8132e451c1e751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713a783704ddcb231c5c959682630f8363205facf1e6bc002207fb570489d3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:50:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:50:53 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:51:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:51:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:51:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:51:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:51:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011970ecf2f315c69c83fa94ac41516957ab5211efc229c8c8c282ce6bcc7724`  
		Last Modified: Mon, 09 Mar 2026 20:52:26 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244c828510b54f631ee1b949f0503bb32e338f1486b9b9f24cdf97930ff38b1`  
		Last Modified: Mon, 09 Mar 2026 20:52:24 GMT  
		Size: 87.0 MB (87000037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86619a29734a49cf3a9e4b3f1efa47e224d7838164aeab891673e112d692b044`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ad578eb2bc1988599f1a1231524fc71a59f271be774a1e80b2b85826d3199b`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fc6863a919b6cd65b067e08077031bc413ddcc4ecf5d8ae7e739e7942f005039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051a2e1036278abaa26b40d2095ccdc779acb9664ed625a71989c6c9654fac44`

```dockerfile
```

-	Layers:
	-	`sha256:306003ea6919e4feb4d60c32821dabcc7aca0e4d85dc549475f263508c0933cb`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8296d74f1cb393acaf99fa44ced797e6b8b7e59bd16273e3803c5eaa0363eb7`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a83096c34ef30d9e9fb79813111f573d051d17882de8c10b57309001b43f4900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262765279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198c16240690949c17f5a4e6dc7ce3909a5ec9805e7f424e3a0258dbd73edcd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:33:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:30 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:33:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5012ce39a9a9ae11cfc01592c6945c67dfcf71ac11d4bf491f0de2e19321dd`  
		Last Modified: Mon, 09 Mar 2026 20:34:18 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b29ea4715a609aa04f8bc24e997725a0ecbaaba901089ca2061f43494ec662`  
		Last Modified: Mon, 09 Mar 2026 20:34:17 GMT  
		Size: 80.0 MB (79989032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e0833e8fde7c31bb7dda07c7d99ce97b682e2b366c00106c0ac3aa1a464b97`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332c55c8e8c28e8c31a3155076294285a06b2645dcdf3086745c75f2e8a1442`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d2ab5616840c78c9f42c7eb86516839407a01359667f8ddd7e08b75b3b1a44c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b7f1502792624c793f22e201f17afd00cc88bfa14448f176d67b92378eecba`

```dockerfile
```

-	Layers:
	-	`sha256:e747ab8819650316390ab15364a6a249c4e6300f50e68eedd0f7767c56fc6ab4`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c47d931b4bedc96e13d5e0af7ed66e5a5139cf82aaa1406add4044698c9d810`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
