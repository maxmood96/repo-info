## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:3bbce62e764e36b49eaacbbf4d12bf11e7e333090f263bc190efeaa55c218cf8
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f28eb764a4fa2a4d9a59db69e2e02b8316d83a6934c2885b0f82134928fd19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249055271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdea47f05a3b1196aa8b94fbfb598b8495be26e067b76889ac01a592574b0a97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e513432e22464bd7da0f7fcd93fdb45bb58bee3d06b2c36bf82260f9706122`  
		Last Modified: Mon, 09 Jun 2025 19:34:41 GMT  
		Size: 144.6 MB (144634949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69861c5063c77015bff506ea216123e0810f3da51f083fe2aa695660a749083c`  
		Last Modified: Mon, 09 Jun 2025 17:19:00 GMT  
		Size: 74.7 MB (74663897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fc634be299b2142601220b3ee7d0d8d77c367a32b15d2ee2f30bff1e438fec`  
		Last Modified: Mon, 09 Jun 2025 17:18:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421dca674e66c2b9b0d9e712ff6d2fc4973740b1dd24dd45f72298fc381cb93b`  
		Last Modified: Mon, 09 Jun 2025 17:18:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b1b9ad7938e183cd4367f3e393bea90a5383e022c79da6489c21b82ceb8a214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71414063d58c18da0357c83371dba639d13333604f4b7cf38e88f0eeed89f2f8`

```dockerfile
```

-	Layers:
	-	`sha256:8d0517402431a98358efba6ace51b88bbb58e20fa105448e751b67b34f9e100a`  
		Last Modified: Mon, 09 Jun 2025 18:38:25 GMT  
		Size: 5.3 MB (5252284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e2cf9b5609a27049b438e81a457b316fbe2f26f8ddc766eba936f4749a6db2`  
		Last Modified: Mon, 09 Jun 2025 18:38:25 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5c3f221300b8947166df14f7f9f77e0b7926322cea00fdb0b114e3362637e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248600499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46fddd64770ea0339c0e8a7cc01d5546b012e213ad1a3c01892dbeb2e3f9f27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa191031ed8a3c8712cc547eedf7bf4ab856214d4cc0076e445d91663c3142`  
		Last Modified: Fri, 06 Jun 2025 12:48:45 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf80e244821e65be1a09cbab69a3d8ee8fd7628ecc71f4003b6a027eb36f64b`  
		Last Modified: Mon, 09 Jun 2025 17:51:08 GMT  
		Size: 75.0 MB (74967355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f174435e639a44b467303a817621f43b33a79533e5b3a6b2c0c8798badad92b`  
		Last Modified: Mon, 09 Jun 2025 17:50:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e513901d64c8d6cc29da831fda489b66ef74c7e13697b10062a492765c4d2c`  
		Last Modified: Mon, 09 Jun 2025 17:50:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aec8bc8f04abf58644c77992d7091c5efba9794302b3a5f48906545fbdb6c282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6613c3f44e23621d6f85e8686d0c1c1df8c7d8210dac732bb7b6d4dc4e0c677e`

```dockerfile
```

-	Layers:
	-	`sha256:a5473e5db78878ad87357d0b25cdb6913b8c807c4a463b56df10cc702de78979`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 5.3 MB (5258053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262b489a058cc74d315f9109daefd3613896f9b19033964ccc3799347eb2aca6`  
		Last Modified: Mon, 09 Jun 2025 18:38:31 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b689ef94da55779c3df1459c3cedf57aac3a0448774ae9e33ac37625235911e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258264084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5182042bdff8f1d59d03fe62d8f0fd77e94685abb703597be9919556c0f3d25c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe2f8a21171dd5775e8651cab944241a8c5250daaaecb5a5a99444957bad86b`  
		Last Modified: Tue, 10 Jun 2025 11:53:47 GMT  
		Size: 144.3 MB (144280520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cdb469457f476e2bca82ad101cf74d16177ac5ede8679f17d72471c44913f5`  
		Last Modified: Mon, 09 Jun 2025 18:10:02 GMT  
		Size: 80.4 MB (80401959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c01d4e01fcb4c5e7560215412608e17b6d1008e276319067382caa8ef61f9`  
		Last Modified: Mon, 09 Jun 2025 18:09:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cc4f94d0a9b6b72c7667ea568f03f3961cd51ce361dc73add4362bde571e90`  
		Last Modified: Mon, 09 Jun 2025 18:09:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3ba03768c3d1742ae87e8c9266cbf633d016c0b4bf7c559e3ed17af6291a724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23194c74eba3f15fcc0d07c5a4cf73f468dd7e968539a1cdca46cec1aa6e2e96`

```dockerfile
```

-	Layers:
	-	`sha256:957b11672d992e79a256a996d5eac2366d58acce3abb4640632a50e3c3b31386`  
		Last Modified: Mon, 09 Jun 2025 21:37:00 GMT  
		Size: 5.3 MB (5256655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dd4de0d23feb699f0b10c9b2acd73243136f1391372b50c7fca8c4a2d7aa5b`  
		Last Modified: Mon, 09 Jun 2025 21:37:01 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:0e67ece51535a5986fa499c05ee126f11fe8dc2b9c8c3865864bdccb99fc0fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240046992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531f093d1bfb654fcc287ac5318814624e5e1052f5a440af15ff00387723c3aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900d390e81d9af67de96fc8c0a46074dae5d79691899bb1c249eff04d790cf6`  
		Last Modified: Tue, 03 Jun 2025 09:02:08 GMT  
		Size: 138.5 MB (138492458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5754e19357bd6bb01a99e2657a53dd0f0719143d07488dd7af26f69d5d7fed`  
		Last Modified: Mon, 09 Jun 2025 19:01:14 GMT  
		Size: 73.3 MB (73308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542c2dffbf11177e6c4fd1c6457d4b705d3611487048a39eac536c851bb385ab`  
		Last Modified: Mon, 09 Jun 2025 19:01:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3027580ef9a3b2f4e5f58cee15b2dd9a5f6b73d298334c9498a6a87d682a8201`  
		Last Modified: Mon, 09 Jun 2025 19:01:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f7b17c64fcf7384d5450bfe5d847b7a87ddd7ab98c21f30946f05d8653e175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ff2fc510d25709e9d9b36b3305baf41167352b20d1a1140a7a3eaeba25a00c`

```dockerfile
```

-	Layers:
	-	`sha256:73cbab8d46381204daf93915c84729135d67ce1da8d6bac481c3df01b0013c30`  
		Last Modified: Mon, 09 Jun 2025 21:37:06 GMT  
		Size: 5.2 MB (5239829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a62f93a69512b99f6bba5ac60ef57596147969a613b216880653a0f20ba76e3`  
		Last Modified: Mon, 09 Jun 2025 21:37:07 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:32cbbf774b0231bf4b4ee84b55228a63ff1730512799ad8c22334b1d7e21629a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239909949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87551c3f4c5f017748dceb4c266e849c139200f20d54ad31b72bb27fd8d6009e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89149c8ddf2f34bc00802d5cec3d426d775f8368fa79ab5455c34c0ba8a1e25f`  
		Last Modified: Tue, 03 Jun 2025 06:17:33 GMT  
		Size: 134.7 MB (134673567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3021a7ded1817ec9473fb3d49b63351ae5bb3ce56394bf8ca8f90fdb39148b7a`  
		Last Modified: Mon, 09 Jun 2025 18:51:15 GMT  
		Size: 75.4 MB (75405721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fde626266dbc09582466b3de20f46f2a4bb93c563f7f18642a4551f7090f84`  
		Last Modified: Mon, 09 Jun 2025 18:51:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edfb87b6343d011e818204026d4cfd039d84b5f880424eb134e8893ab562652`  
		Last Modified: Mon, 09 Jun 2025 18:51:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c0d32ed573048909cac098f736d4ad7680627f88751eb0cdcf42f0486170b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db07566895b7a6bed5f208bafeaa483d379c26c31a3c70250b1ee3465bb48a1d`

```dockerfile
```

-	Layers:
	-	`sha256:3540f5545ed89a14875a54ce8310b3250244ec1c7fe9b4b043857d2f32e37016`  
		Last Modified: Mon, 09 Jun 2025 21:37:12 GMT  
		Size: 5.2 MB (5248208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f228ee5708543d8a91d631f488d5f54c97d99dad1608fe8a6f934757c25698`  
		Last Modified: Mon, 09 Jun 2025 21:37:13 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
