## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:dbed70947f726d156d95cdd303cf0341d0a1403c948cbb200351ca620f2aab16
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8f8875b343a78011f1ef98cae353826906e2def01499332ef2a338b2574a47a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284780536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7006564f520fb21c04233d4ca3fbffbab8df5113a53e5ceb76ae916cf2494a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:49:07 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:54:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:54:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25284de88594517d85a7360eef895de970f33043b86caf252b64664918c3e557`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13b6d39cb9bdb1b333864816de7d057050d81a654f577c18cc3f7bc905a94a`  
		Last Modified: Thu, 16 Apr 2026 02:55:08 GMT  
		Size: 87.0 MB (87004259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6da97750b4474f32873d40a42edf8f16e673d6c146689ed8001604f71fe9dbc`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9273f10bc056901c484965125ab10fd2a2db64ce330d93c2326343dc2e647`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8948b02b2fe445ce60b7a01c243ed48c2d2b2dbf848d0debd568998c9b72091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1697f6799032f114f6911d6bcc86073c1489952e7bc17b6f6cf3e148c5a36a3`

```dockerfile
```

-	Layers:
	-	`sha256:36394c18e098c6630ec748a9111af6f4bf17abc2a21f954bffb3d4336141a45e`  
		Last Modified: Thu, 16 Apr 2026 02:55:06 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b3fc1ec23a5f010f4304bd1f947bfa3dbdb5c7383e1e9115a162c07a6e8a9a`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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
