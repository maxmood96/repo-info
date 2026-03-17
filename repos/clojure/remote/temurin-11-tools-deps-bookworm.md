## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8e1a596d4a9cc81d07a1c9f778415e0d6f8bd5b639d41cc7fd0f420865c55931
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a8f0c1e4077016001250906c8ab51bcb749ab51616b71aa714291898e5a60c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275473379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1b04e0b75c4fe3695323319b4be092d31da524ad0ac29655f1b7af4051103e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:57:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d947a4ddbd004f6a81a71f1e541b7a2b5349b44a91e343ce419d5c46bd7d2`  
		Last Modified: Tue, 17 Mar 2026 02:57:55 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37904e02e0d9fc1dda8d34082b13f4fddd5b11c8f0e1d63e7d6365b4a88e3c5f`  
		Last Modified: Tue, 17 Mar 2026 02:58:00 GMT  
		Size: 81.2 MB (81177238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d02b3e8ba4c5804efa98a98bb2faead5b1c646bf1568c7f564af234ed4e80f`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2c790c97f5f82f20af42c69977402b32e99b410a354c65781e01dae740ef66f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652b5e7f6dcb36457d9ea22938ee4a306c664ac33a99447e3384bcf7c045665a`

```dockerfile
```

-	Layers:
	-	`sha256:744a5c3f7766f0a54759d73d1fb43314dd2e9a2d08b2dc58581a7da822b3cb32`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18fd2424bb839e01232f9f01959f134f06f5289b4be7609b2705689779e60684`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45cc589d3736d35e75bef8cfd5717b9569b12cc7a32733239aeebaf737fb202d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272032061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cbf090d219aaace26b18d638ed34faa3aaa97e4852c0e747499426e3190503`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:50 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bad337430304e6581e9cd2ea833d27c5521ce94738307e3d500f4962138bfd`  
		Last Modified: Tue, 17 Mar 2026 03:02:29 GMT  
		Size: 142.5 MB (142500050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2187f4814b1ab36cffc556b50a0b29a1d194c5789b99385ca288683f77ce22`  
		Last Modified: Tue, 17 Mar 2026 03:02:28 GMT  
		Size: 81.2 MB (81158336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202073a776faf98f67b4eb847aeb73341c8e76eb10e2d702729ee37354e915c5`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d5e16dd0b3662c258b5d2b51898a09fe37faed42593ae43775c82c1cf0aab303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b913baa09d3cb6967a8b7a93d5d85994a1674be5fe195db737a0f11f56faf39`

```dockerfile
```

-	Layers:
	-	`sha256:64656219aafc9e2f10e46ecaf52eb862a20ac2ff61c5d1d402ad8894045277ec`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6bb96914d23978f65e486ba5fc38ea155b90f307c79a6df0805cfdde12b8512`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c3207a994fe27f0afdf26a7c67574d4614e747354de8838e14137e1dec994881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272335634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e69f308d19f827e4bb5579b4ed0ceb9ab29a8d50475a6d32535b47b6f9178f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:45:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:45:39 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:46:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:46:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:46:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fe91e8aa4cbe7900d756836850a26915a6e3622e92a5a9e11bd5b8b6533b9`  
		Last Modified: Mon, 09 Mar 2026 20:47:05 GMT  
		Size: 133.0 MB (132997814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8395c8c208b01518f450d8b93812d961b3869c25451ced7715ba07c6bf4db7`  
		Last Modified: Mon, 09 Mar 2026 20:47:03 GMT  
		Size: 87.0 MB (87000376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1fa11ab6de7d28634bd729586d88b88f105d80b9449a05b591cefda17e8847`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:01779a4c5ae23ced61b17068e8c784f613ff955c69addcffe0ada9a301c4128b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b8683ca881a3658b36b1aeeeb8511c29dcce459c415e9de328322f3a63837c`

```dockerfile
```

-	Layers:
	-	`sha256:8ec6a8bafa1015c19263674aa5c682f257c90250504b57b481152c6e645b044d`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2857e7030a4791ebe4d06e9d26710b14b5b8c46ce6f6a38918c5626156aa11c6`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7f27a02cc04234536aa19d4c6349d0715724a689c8464005bcc3badd4756caf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253699023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b4bd4764528e5648a16e11247a1f40291a23e98c3ef9c4a48dfa6deebaadf2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:13 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78455097ab053fd4a095369b6037e8270ed42dee2c12d398c3ce66f2d955316`  
		Last Modified: Mon, 09 Mar 2026 20:32:59 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b70367e0508c833c3d43fd2e1090c13fc6ed4d449a06b77834a13ff680e9c`  
		Last Modified: Mon, 09 Mar 2026 20:33:09 GMT  
		Size: 80.0 MB (79988230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cb70fb717bfa2edb74de6384e733afdc2169bb09b9dcb16b261d5cc1893ed1`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:968d67a6a7e5717b56cabaac16b066e381e749507895ca4940174c3152dbab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90a9575e50c28f9f1143c86d8b36e64723c7647d7dd57d940276ca175ea0f9e`

```dockerfile
```

-	Layers:
	-	`sha256:46d3a718b770f046837f53c5a1915388e36b0f635049341757f8669cf31adc93`  
		Last Modified: Mon, 09 Mar 2026 20:33:02 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e2bbaa200831b12540cc29c9366b511767781d1638610384e179cd779eac87`  
		Last Modified: Mon, 09 Mar 2026 20:32:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
