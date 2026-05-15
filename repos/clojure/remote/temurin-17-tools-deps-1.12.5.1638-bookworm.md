## `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm`

```console
$ docker pull clojure@sha256:264008129c65e237823224832101d95c95631c4a758aae00192a73cf25252852
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

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6e6cefff3ca3218884955b05ee91497602c80cc7a3c53b267155b4df83896eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275608652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb3568cc24330c64153510f25419209767fc0df846daa301dbb07f399a01a09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:07 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:07 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e4b07698f1229bf43c5188d8329829ee0524d7f1b1578a2c1a23bd97462f0`  
		Last Modified: Thu, 14 May 2026 23:35:41 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c45d1041952966677c3c407ab2b8b8bd02158486b7c667ceb93f33eb6568e29`  
		Last Modified: Thu, 14 May 2026 23:35:42 GMT  
		Size: 81.2 MB (81213454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1807c7081fa95eb48715d82fdae5df4d69671264cfb17676ab5a2103e37d6cc5`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f932ac13ba9bd811f80564dbea83562499d395de97b79b27827230d51f724143`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ec259bb1ddadc105710d36f728110ce3dda2f958c3d7f9d904f16966f0d21f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32defbca83017f75cb2006bc82fda74bf9ebf72e664c331e35f93ce50207a72`

```dockerfile
```

-	Layers:
	-	`sha256:1bf3b273f4dac67c84625e52b169b22677c9fcf8f000b085c283075999409b6d`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 7.4 MB (7378927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf13620103e8d99b1eafbecee4e84ea389bd7ec62c8796213f4ca22c64c8bc7f`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:756c1ca7cc6d70bd8d7de60bfc3ccdbddfc321a5d09911f8e313e5be9da2f4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274294382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68e7b36da7c6881b14bbf7d65736bb332aea484924c61a62ac112b26f620435`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:57 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:57 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f885891b5b2efa5b785f926defc4b2d2212bba5db33c7b1eb878f33320c540`  
		Last Modified: Thu, 14 May 2026 23:35:35 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ece98e57271f8be27e49c2ecde51993b7c9046c5ed5fc50f1aa897cc5f222c2`  
		Last Modified: Thu, 14 May 2026 23:35:34 GMT  
		Size: 81.2 MB (81195830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee8925325ac31e5f166b917592faccfe52d095075902c71e1e5d4856d04d88f`  
		Last Modified: Thu, 14 May 2026 23:35:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcaaf511c96066805a2586666f7e4cc2f9ed4ba58930682d403b508eef0d10f`  
		Last Modified: Thu, 14 May 2026 23:35:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:85f31b495855a2bd33cd0c743bc39bb08576442fd212656d919f0482cc168bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a66ac62af7ac1c525a215ea01b35491f355a6c8332330d514515f700631ddcd`

```dockerfile
```

-	Layers:
	-	`sha256:47b1fc956274eb4fa0b2bf7ed7780368c97139c464a47ba169b17903f8be3924`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 7.4 MB (7384690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e77d4534e2b1ed11a847f4bc8f49fef60be158103fa8c9cf8ae19b8aba74e56`  
		Last Modified: Thu, 14 May 2026 23:35:30 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f37b551e590c72957d17fa560d71311a7b6b785cfe29045791d010e5a9431aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a352631e1b522dec3192851f6dd320ce62199d7614555d1a233407d7a5d3ce5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:22 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:30:22 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:42:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:42:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:42:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:42:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:42:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8690ec3700a5aee074ea4c1951ffc72590a2a8686be7918dee225def8496211d`  
		Last Modified: Sat, 09 May 2026 02:31:26 GMT  
		Size: 145.8 MB (145766181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c13e500bfad8ad4e1983fe5c313384cb1c6a4f02bf0294b273159db381f9ec`  
		Last Modified: Thu, 14 May 2026 23:43:24 GMT  
		Size: 87.0 MB (87033195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd529212686082110bd29e37d105cd923ad6a1b63dfd53c4ecb8b336b3413a9`  
		Last Modified: Thu, 14 May 2026 23:43:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb9b680131b0d0a2b630db0cc9196fdad5bcfafec7a06efe7f3c3982b4a8ee`  
		Last Modified: Thu, 14 May 2026 23:43:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0e41facf136c8d0976d6f003dc23cc1d69c7d9842cf23d5fe7bf8f9cff38ecb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d012e7c28476a28964d68b1082c6391b7cd1c8c5dfe8c0f955124b8def7bc2`

```dockerfile
```

-	Layers:
	-	`sha256:b9bfa07175860f00d08e6b74661f78ba8c2a4bd414d9774a9a28dac333254e67`  
		Last Modified: Thu, 14 May 2026 23:43:22 GMT  
		Size: 7.4 MB (7384143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b479c614026d9c6b7af653a3bf30c41b0631870e7180769b29a4326abfeaf8`  
		Last Modified: Thu, 14 May 2026 23:43:22 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a2177d58cb63459e327828f800ab33375386b50168fda1e4d07b88f87d47e24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263084278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bcdc62da67dff9cb7356e47dce67c0eaf2d142bbab0d514684a9d3cc3847c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:37 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:37 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:33:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:33:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3b634a56c45e9e1d53fa1e2db314dc6d82097700cd89f7085ab8cb1cd0dab`  
		Last Modified: Thu, 14 May 2026 23:34:20 GMT  
		Size: 135.9 MB (135910383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b076892c52accc6bf09c845652c15ffc0badf13cda849df25a4570f1a5ab`  
		Last Modified: Thu, 14 May 2026 23:34:19 GMT  
		Size: 80.0 MB (80024826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c66cba71310dbd8a52d56ee0526a374432988d39d08b5cbd30ccc3be2cec391`  
		Last Modified: Thu, 14 May 2026 23:34:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb5742d3578c07d290d1b344c6dd0b5ca558f24355fb17e070c705c19d482e9`  
		Last Modified: Thu, 14 May 2026 23:34:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2defbee9c6b33030ba899043ae7f62f522560ebdb0c4ea96b885eecb22b76cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251f9edcd54056b0af6d8fb6fd09925b5d11b694f5b6690beb128e2842a4755`

```dockerfile
```

-	Layers:
	-	`sha256:dad10351efb984a3226b87e2cf7c338d83017dfa8610bc2e47afc7bfb13ddb3d`  
		Last Modified: Thu, 14 May 2026 23:34:16 GMT  
		Size: 7.4 MB (7370246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d7813aecc0da6ac9be1b22a984240a24fd1a378584a321b630f5cb21389240`  
		Last Modified: Thu, 14 May 2026 23:34:16 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
