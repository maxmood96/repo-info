## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:de936bdd451574bc8da122850298a0e29d1cc4d7d1f1a7c295f6b209fce319dc
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:16343a12ba203ca9ce1a3aea9a1d9ed44014e79c30acd8831d66a5d00ea75a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275284917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19423c1f8e1cbd5898bcea661748cd09983d33dfd94512ad8b455d002442de9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:18 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:18:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:18:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:18:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abec0a02efd54ba6909d6a0d2ca93234cee0a51fcc2409a318b67c57a8e6f881`  
		Last Modified: Wed, 22 Apr 2026 02:18:58 GMT  
		Size: 145.6 MB (145628741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429fcb477a9848585fc87c4212e77812f09856ea5e4d06b3f6a664cc9c7fc1b`  
		Last Modified: Wed, 22 Apr 2026 02:18:55 GMT  
		Size: 81.2 MB (81166508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ea1541644b90fa1c31d74e86dedf0880b3d14cd58404079756e8a8446dd5c3`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77341044c7953fac0968544ff03564887d8abb16f714d77c9593d9060e451589`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7a70ea1a5360eb60b6378ffc2e76e4da433b2cec90fb86b496ad1d4d5144278f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8a4ccfbd8c24f6f0734f7c5b186568a4c0e16ba09b8f4ab6079bd6951e12b6`

```dockerfile
```

-	Layers:
	-	`sha256:9b8c0784ffa34242f7a145ece613c760746d744a1b2517c7d46124f9b58ef30a`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd5c90ea7f7479e795eea391d893270c72a3a6f7491d5f30eb0d3e1b0ea887d`  
		Last Modified: Wed, 22 Apr 2026 02:18:52 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b03514680ccf9377b395ab5c70ea8df934ee49712082055011a46a5ee7b55bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273984672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8842168570fc19f00827dc53648cb789a51c099f3be45355404e9ad859a6531`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f06212b35e7c8240654dcf2ddc43667ad7c3e02ab33bb3114bb74e937ce57`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 144.4 MB (144436253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c231a882d84843f3bca9a8340234579cfa12990e714faebcf9bf9a0fa10fb3e`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 81.2 MB (81174308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab1311176535a9aa723d7bee993e4bb3571074936150d65f84bfba4afcde8b5`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93c814a8a29eddf6c61c598c198eeafe3329f8b83c188f8db0a075c100656f3`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad53942beacf0b3f6f5a26ac8241fa453cbf39ddcd1268797fc6775105b9ae49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40374b533a25d33dc3d2f914b35bf395c0e38f3dbad5d0885a1acd5c7c92786d`

```dockerfile
```

-	Layers:
	-	`sha256:7e60b15ff25ab685d385f079a620eff97138f74b1fe2df4394432e8f37151d13`  
		Last Modified: Wed, 22 Apr 2026 02:22:17 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602c7d1e30ee9a1bb83fbd30cd288905390bf0f0588b184bd74adca6b52f2cb2`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8072a41f74203db6515ed443bce4a95f382508d3b209e281827aeb09562e7ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284780134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abc3a0e4da3b8fc53ee07f272a45095e3433ac5dd4c2a3ff2aa5ffd7fdb3182`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:28:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:28:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:28:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:28:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:28:59 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:33:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:33:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:33:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:33:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:33:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2379272adf5765a18fcf1cf245cc1014b3b9f87fd7dda1a133770fa3adeab7e`  
		Last Modified: Wed, 22 Apr 2026 08:30:30 GMT  
		Size: 145.4 MB (145438261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358e54619e9880835b721d017fd7822d34286afaf3b89e11c54a4b2bf5b08b99`  
		Last Modified: Wed, 22 Apr 2026 08:34:26 GMT  
		Size: 87.0 MB (87004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c35d7552cf3210b320f3f5dc6eebddf907255c66e113132993625bc87aaf5fa`  
		Last Modified: Wed, 22 Apr 2026 08:34:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba56fe4be199f0c2ee038ef6c78562544a32c9065349c05841d827fd0bece0de`  
		Last Modified: Wed, 22 Apr 2026 08:34:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:857238f6fe96abc11a473b588f509d18fdb86ff1df15f264dfd5806ffcc6cd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3701fabae4ceec142dfa97edbcca94bbdeed3d3fec590fa6d12cf4db230a0a`

```dockerfile
```

-	Layers:
	-	`sha256:a4005459c50dd9d0c6699619633a8e00202025a3c6c6b17611bcaa770dea2626`  
		Last Modified: Wed, 22 Apr 2026 08:34:24 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5257d159e16693e6e58cd18206e9df1c06d585359cd1254b229578aae62b04`  
		Last Modified: Wed, 22 Apr 2026 08:34:23 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:930790424c879305462c53c6747e04d4bc20cc625a880fbf5a2ec6e5201d607c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262755676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a102c6ae6c31dd7a2ba56598fecb330a13906e7a4c25c72d0cd7a6bd6555ce3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:00:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:00:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:00:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:00:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:00:34 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046564bc8b79a0be58c4ba63f7db980f118576e0890ddd62ae27ffc38620ab70`  
		Last Modified: Wed, 22 Apr 2026 04:01:22 GMT  
		Size: 135.6 MB (135626974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f44bcd7eaa59aad360bebb2fb7ab02d7ae3378d87ace3f8f1497344e66de7a5`  
		Last Modified: Wed, 22 Apr 2026 04:02:31 GMT  
		Size: 80.0 MB (79979694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef038e6ce13f47f6b492f55168aa9e7867cf6f033e913ea8f808938b92c8e2b`  
		Last Modified: Wed, 22 Apr 2026 04:02:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180a86c44e7b88984a86d9e7b27d9457737816533868ca15cbd0ecb5cf4b6138`  
		Last Modified: Wed, 22 Apr 2026 04:02:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3f62e3c70dd5f28c80654cf9d8bcaccf45be9f2dc8cf9eafd2a8f38e8ad4a680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431b37e4a2bda333e77881c83e8a7f598dfa80f4479285237a037a94e1290984`

```dockerfile
```

-	Layers:
	-	`sha256:2e068d6f9252773c30b133c805051f25fab3a741a0256b0b82fb3da5a1522b69`  
		Last Modified: Wed, 22 Apr 2026 04:02:29 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1cb6d8589386e301f2729410317ba88a9c5566478af859cd00fa3236c85fe86`  
		Last Modified: Wed, 22 Apr 2026 04:02:29 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
