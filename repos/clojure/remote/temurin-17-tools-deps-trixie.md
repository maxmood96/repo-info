## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:af3c20b4a42c89cf6291d2df7e0ba325550082949f4124cc8b4afc1bcd44c2eb
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
$ docker pull clojure@sha256:f4b5ac60ca99f021a98870a9699723cd4e48d31e6454cc0f3b1dbf510188bf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280779200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397c8ba2343fc0f2647c0f367d6c6c025526fa6c80482b99e28fa6bead04234f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1e5be7273d6b722c905e2a65e2ace602f8038be40c8073334ea51baa7c161`  
		Last Modified: Fri, 08 May 2026 20:18:04 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfd5d1e4f94dd4fabf30e3e20a4594cf9ef16febf405043c8e39838b4e4d886`  
		Last Modified: Fri, 08 May 2026 20:18:05 GMT  
		Size: 85.6 MB (85570351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcc125aaea140ea64aa4e5a7bdd92ebc4ad85b442e788708cea3887dbd956f`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d046c6b8aaf1cd3a6c47ac405618e2a77296b1a0738d2b5d72a2d2ab23162f`  
		Last Modified: Fri, 08 May 2026 20:18:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7f38136e468031e1b093d474bf20ea1f31312a93da09612f72d8f2c85d1b7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9d63f8c91638c2f6ce9493bf33b0fbaaaf6d20b80b7a549bad96ccd2d0d48f`

```dockerfile
```

-	Layers:
	-	`sha256:fd1a33d868645f1fcdd1857b8c30405e1e529cf644e7a4d9d1a7c4bdeb411fb1`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 7.5 MB (7471348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de2eaba3b842425786573faf14489ccff3392d346cc47f9084ce2998de4f3aa`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c584b93b17c88e756ea0b6588cd2f5d6d965be410d606990452a76fb3853b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279778487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b291a88210676dd5034063c6fa1f4d07e1d5bfb32b5d2e22ca709116ae2df5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:43 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:22:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:22:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c836eb6329ea86476f06021e23449f5fa9f1b68c20a0d015905f1276e5487`  
		Last Modified: Fri, 08 May 2026 20:22:24 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc6fb48129cc6ce781f623c3e672eea574ad8e052a8fc5264d2791d5acd9f49`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 85.4 MB (85383665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322e1542faeed097ad9574fb7ceaed96732442c29b4dc424f47d76231d97559`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e9a8bc27eae71a13eb30dbf6793c17f3fb07573e7ae2718fe2f7227fce2f7`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f40bfb794baf319d6bd8cb9834df9771bd6c41f71f693f0415742cf2721b0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bae396feb5aa3d529a6f77656a7330c6dd57c12ad566b6501b2f3730d2ec971`

```dockerfile
```

-	Layers:
	-	`sha256:8189bdb81b15edeafef3d07a5038c7759215ad959bc2a1b08d30c45de715f9f9`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 7.5 MB (7478378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ca6be1961a79e536f34602ac98310efd335ef6daef30c7e9112f7611f8543d`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:be12f2ee0b1d4d74c40fc85c48efb5c00cbfed3d4e024c680ba708490603771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289876768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc2531f2004aa97091963b9177c3bb035761fa2bb08679684740ea3b85dd937`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:45:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:45:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:53:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:53:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:53:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b7eb5aea1a56bc2fcf2ec92c34b7b899cf187331f6afa218be284e921541e`  
		Last Modified: Fri, 08 May 2026 00:47:15 GMT  
		Size: 145.8 MB (145766229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669bd8c7c869f8fb3755cbf26d6676b40596ba3320dbd286d8f4279a611e7644`  
		Last Modified: Fri, 08 May 2026 00:53:56 GMT  
		Size: 91.0 MB (90986515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7e6365702509ead0cc28131f0cafc6b909c175ea52e9ada76a8f1237f1a7e`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df182d32e5646108ff40e0cd71cdd6d04ac8797b182504c8f4c63e6e47d8039`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd217bba69c7dfc436ca1310f2f112e7b7f791ff88b8dec3b697021e87792428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f041abd609de7fdcec916726d1860b4a6df69e8834d358d8204cf7fe770bd1`

```dockerfile
```

-	Layers:
	-	`sha256:e56c1a3a49ce0e6ada4607c10a2d48b311ea239e9be7ba0599a4ca2b06ed299c`  
		Last Modified: Fri, 08 May 2026 00:53:54 GMT  
		Size: 7.5 MB (7475769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3287daab11ec68bfff43bc1ffdaa01ad986dcd147b5be5694d933e5f35edd1d`  
		Last Modified: Fri, 08 May 2026 00:53:54 GMT  
		Size: 16.0 KB (15955 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:5f77804697060f1c518ca7733d34f110dad97e3e4520b6a1ef4e92a4b9ef4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274921312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a966d011554534d39f899f928737ef152c44b22e67c7cfaccc6b192d2432a447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:41:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:41:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:41:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:41:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 17:41:32 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 17:57:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 17:57:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca059398ab85ec46154b4adc01fde7c5c787818bd1a043bdd89c080ecbd2e3db`  
		Last Modified: Fri, 24 Apr 2026 17:47:36 GMT  
		Size: 142.7 MB (142662892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafc3d45da4972b3524556b66cc3571fb9129ecf9fbfc391a903a4d428cfabc1`  
		Last Modified: Fri, 24 Apr 2026 18:01:48 GMT  
		Size: 84.5 MB (84459162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d032f5acb1f07b3532d695c592bea544200b56fb76a4adabb87d2224d820aea0`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc17400ed1407e8d15ef31946f0851e3c8d37fdeb01cb09503f9eb60660770d`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d996b2878cb60199394c2c2086b42dc7677a2617625dd86834400922e449584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5487c01c76cd2fb12f6e78d2b96bf113573d7a31b8ab2df106449e810fd7d087`

```dockerfile
```

-	Layers:
	-	`sha256:54b4470a90a5042c4fcd6127654c711015e87c4d98de367b1b26647d9c3e7e4a`  
		Last Modified: Fri, 24 Apr 2026 18:01:37 GMT  
		Size: 7.5 MB (7456717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6553cdd66f9ae918428a7e3d437d877e9cf2400e081afbd90e64ae11fc7f6d9c`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:373c16b2513ce61ee08fd1a1674939adb310b7698ddfbdf06a188c3201b6f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271828475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680e71abddec07e869bfea629c38ea3cec3c04de5118993dff9dcf89960425f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:15:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:16:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:16:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:16:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:16:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:16:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed7aaeed1c65fcc4999767a473cf745af3bbd97738b57ccdb46296b8107390`  
		Last Modified: Fri, 08 May 2026 22:16:12 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e43cf2b31f1549e9bdca4f4f22e9b37f459bf18037b7906a5a7ab1b26b998f3`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 86.5 MB (86544695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a1dd646a5ce2cd6d2630012fac61bcefd007e40e349cd4e8a3b57f6b94e9d1`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14d4eb6cdb9e27cb2eb094fd5cb59b6cbf08e9ab295bac4ef2783e261c9e15`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:043f73acb918a9453d73ae498928298aef1eeea96f4c086b749c6453b6d9c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d076828f1542c381253ea089b23e356aefaa62c23a6267f86fce08841a87318f`

```dockerfile
```

-	Layers:
	-	`sha256:72f835909a2e517944920d46d7f7f6beaa5f54acd7b0f1551e296c93544bcdc7`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 7.5 MB (7467270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c872e26b8ab1f8bb976235e5f6b3bd585c6862c091bb277174542167936b0a48`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
