## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4196208701c6c95f0a30e9ee7c152142934b18210fc2464526dc7288931b5f25
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:894de015a96ec051561e2dd9b56e31cdd0bba7227a6b784e8188449b46cb4db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280464740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37176b0d92e87d506be57f3288b32587af80e87aee1953518f11c9598e7d5907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:52 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc8e19eec260fe634438bb83a7c2ba88c3635c1f7d170b3c2083343bc8a23cd`  
		Last Modified: Thu, 05 Feb 2026 23:05:31 GMT  
		Size: 145.6 MB (145628508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7df75e4c77b9cec59405667add6544fb083ea2b436f157f84cd49d8ee5eb93`  
		Last Modified: Thu, 05 Feb 2026 23:05:33 GMT  
		Size: 85.5 MB (85542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca25600c28456c8ff2f96acd62e7aa4d7659e08a1fcee5ae373343d4247da1b`  
		Last Modified: Thu, 05 Feb 2026 23:05:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b157df360a10fcc08da9d76777ba5db75a2cb7452ce78c151cb3bde55bfee`  
		Last Modified: Thu, 05 Feb 2026 23:05:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12928e30e748d40b896b14d67c3bb43175d8ec4c6185210926b748de0dbd833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10730f701202a0cad0bdfee33c1967fba5dbb77df5a0abba6c21a445e94e64af`

```dockerfile
```

-	Layers:
	-	`sha256:8943e26bc2989aecdd7a324ac28799ad8a3926393b60229f1fd5bfbc782cbf53`  
		Last Modified: Thu, 05 Feb 2026 23:05:29 GMT  
		Size: 7.5 MB (7469080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597d3d2ed9a844b5d5f8472232d023321e58ea44046fd0e19d3cec6ab3c5ac4`  
		Last Modified: Thu, 05 Feb 2026 23:05:29 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74803d929f9e1e739f9a7f948ff9f6d7483097e82284fc50b148cd7c02a196e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279450305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44bbd45cb0f400b6ddc102220cc3a7eb360b01728b0ee7dc055e183f1321842`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:05:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:06 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a1569030170a2048665bfb0a42b6e258f3a7b85cabd14c56b13a0a8522ec3f`  
		Last Modified: Thu, 05 Feb 2026 23:05:41 GMT  
		Size: 144.4 MB (144436235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4aa372c862bbc9c72cd611f2ed4e8ee1c859865f126b203d3669783a2febed`  
		Last Modified: Thu, 05 Feb 2026 23:06:29 GMT  
		Size: 85.4 MB (85361012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088c8f96dee679801b6e2e7c20376425efde50060984ad18199a6316429995c2`  
		Last Modified: Thu, 05 Feb 2026 23:06:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0b37039a9179aea3536ea785bed767abf2e86a87095f1c140a3878df2ae496`  
		Last Modified: Thu, 05 Feb 2026 23:06:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3df7e9bd2153b4e0402928f863fe9770c01b4e1e81f563151456e364e036682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90be4d45745a029acec3b9975dab18954f76affa8f76a258a5ce7750435d43aa`

```dockerfile
```

-	Layers:
	-	`sha256:4fce9d6381b6f1eb2a3053d94b2f9959fb67d471cce2bf54c0339550214433f0`  
		Last Modified: Thu, 05 Feb 2026 23:06:27 GMT  
		Size: 7.5 MB (7476110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce30df6dca018858573e0d3c8206f6153399ad515ce6429f14e09cd3c7e2c282`  
		Last Modified: Thu, 05 Feb 2026 23:06:27 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:90ab2764fd1ef2ee352d2243f18b1087268edf3cc69e0e25abb038323f70c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289498818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e70b1271d04cea663786b21c0b7cd0828df8b4599834bd546b7af6b198987d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:25:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:25:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:25:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:25:39 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:32:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:32:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:32:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:32:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:32:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806148462c30ed1bfef62eebe515a501af99978464a4710c612e54794c9190dc`  
		Last Modified: Fri, 06 Feb 2026 00:27:41 GMT  
		Size: 145.4 MB (145438280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2132f8b0951e5d5e5128ad6f6589ceef0c0f57d948bf535a3915914f43c3b2`  
		Last Modified: Fri, 06 Feb 2026 00:33:42 GMT  
		Size: 90.9 MB (90947382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f7a4bc63242979f9837e5153c2b2b2112983b766e97692e975dbe8f1d5968`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6630d7a0a5063957f0e08aa33a2c9dbd548d96f7234b4038196cb67b7dd7a5`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7d56f21f93f1ccfa417f4105384631ddda32ee398411c119646537738a8ac67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa24bf2157a84f039f251f6848afd7596b3df7b6028d8a7d3bfc97c3b71059f`

```dockerfile
```

-	Layers:
	-	`sha256:129dd89792f7bf96c56ecc2c2f9083da706a0de19b22f17cb106fc0581ea3dc2`  
		Last Modified: Fri, 06 Feb 2026 00:33:39 GMT  
		Size: 7.5 MB (7473501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba29271356c3a85df679bf3ff4fe1265d63a1086e70a1e3629e7c80377f3592`  
		Last Modified: Fri, 06 Feb 2026 00:33:39 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3c88d6b7321623859857f5b9dba3e58168e00301f94c2466104366ef24b88e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274092597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ee26c474f16823d71334116058b43484acb369e539419e0141fb57536468c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:13:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:13:51 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:30:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 20:30:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 20:30:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:30:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:30:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8715f0f462c27c39b67aba65879f61c571d7691a6bbfdcec6aed27eeb28ae68`  
		Last Modified: Thu, 05 Feb 2026 20:20:41 GMT  
		Size: 141.9 MB (141889578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52a92c3f1cf7df000d360699c6a93faa66ae57dbed264d27ed1e777a80f29be`  
		Last Modified: Thu, 05 Feb 2026 20:34:57 GMT  
		Size: 84.4 MB (84425215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963686b21f4771a1db2faf59ca449265912c3fec33366241849bcc92b457751`  
		Last Modified: Thu, 05 Feb 2026 20:34:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0100d91163ae1abe7d6c612272f7c9572665eaca0f533283e79faa461d2023`  
		Last Modified: Thu, 05 Feb 2026 20:34:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c4e1de9c656e2a2642ed3e4051a1dbb07b6d2ee9fbdecbc84c083e2cc4889e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7469624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada5106b733380dc41e7e5e986c647355db211f0f1923104e754e583a972b363`

```dockerfile
```

-	Layers:
	-	`sha256:69c1722b1b12e06bd1e78f905747521cc472e7c71654d388a9367740a4ce21aa`  
		Last Modified: Thu, 05 Feb 2026 20:34:46 GMT  
		Size: 7.5 MB (7453824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6259cc4b21b566205ed31c073dbb5f9d82e16bfd6092668e1b345224064e6eb8`  
		Last Modified: Thu, 05 Feb 2026 20:34:43 GMT  
		Size: 15.8 KB (15800 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d5e44a4a448fc7f7b6103d27a86073e3c08f4d57c1fbd9e2c508c3b78ddc4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271494097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13519219fbf5ec9419c976bc37061fcf0f0b3234cc80c7410dc787e011c27e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:02:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:59 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf389a6a5e627a977a7dfe9ebcff8ac8e498c97e8faf5da41be1750104836fd7`  
		Last Modified: Thu, 05 Feb 2026 23:03:42 GMT  
		Size: 135.6 MB (135627054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4099cf16a794212f94799fed73f1a08ad63b9c71bd6150f6bd84ad9027227e3c`  
		Last Modified: Thu, 05 Feb 2026 23:05:31 GMT  
		Size: 86.5 MB (86511623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd89c78719c2169017dc402c66e3a9b15ac16d1d48ec5cb09a3e3dd3d2806e`  
		Last Modified: Thu, 05 Feb 2026 23:05:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181d8e91a39a1dd39112f85265de3e00c3ed2967f403bdba44347fab8c329f6`  
		Last Modified: Thu, 05 Feb 2026 23:05:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b80e5fd54ff7c05c9d6c98c3a3b11f5274c0596a67063b1230952bb227cec386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80364b6e8f98c19e0e0dabfed936bec8e7c3e7126f59742ace44ea4aef01b3b1`

```dockerfile
```

-	Layers:
	-	`sha256:eb782de09e289babddde0dd0d05edc4c1ffeb415f0366d818801847afe941128`  
		Last Modified: Thu, 05 Feb 2026 23:05:27 GMT  
		Size: 7.5 MB (7465002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81d749cc28b045fea86f9aa1afabed6d514fcf0821888c23a6e6de150e26bd1`  
		Last Modified: Thu, 05 Feb 2026 23:05:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
