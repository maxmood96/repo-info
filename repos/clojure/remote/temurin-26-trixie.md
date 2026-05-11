## `clojure:temurin-26-trixie`

```console
$ docker pull clojure@sha256:b54cdf90d39c849968fb9cddd084b15c08cc121563a08775c5e5303927be8ea6
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

### `clojure:temurin-26-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d0496b6603665016ac4ab4360fb9fab33ac116a9f30ac3757369c798bd50e9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229330045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6541b2600e0bd71b94d9d41df4b0d606e6c25eaf18884f29cfcd5817ef3f42d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4310083c0e7fd8146fe30b81bd233a1897232746d35d200a873f6f185019`  
		Last Modified: Fri, 08 May 2026 20:21:20 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113973e6e2d76d16a7f07bf40417d246eb96080745f3907fb4125d57fb46930b`  
		Last Modified: Fri, 08 May 2026 20:21:26 GMT  
		Size: 85.6 MB (85570996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325fc435e87af856f3d88fdc0b4c344da5b15d12ac13eeaade4fb6f93e541805`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359f865658a4effffc24480b9d3aa202a3cb747f06189e1aa417ecbe1d0569f`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d1c30bd59bb8959e5dd64cfeb21a328365ba653a9ca1c3329097f54ddc58955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509a2d473923d60d4dd6784a9b02a0bba7b7304e21d346bf93b78692d8aaf8d0`

```dockerfile
```

-	Layers:
	-	`sha256:fb185df010fe16def5a3feadf28a8d687930191bd26de84ab8a8abce81b3c8cb`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 7.4 MB (7436225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b18deba44db2c5a65ec4730080580bcc88407dc678b85f6c4e03fd32408dcec`  
		Last Modified: Fri, 08 May 2026 20:21:23 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0015699f5d6887c7cea696b5fbeb77f2dc1fad02fe522aa422a6787a8cc8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228449176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73be87674a1327f33f304d364f98bcafe5d637da55f6d07f5571aab8602b54ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:25:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:25:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:25:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:25:11 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31131f3dfbd3941589dfa47f6054d400d6e0a0837286c97057e82f3d99795b8`  
		Last Modified: Fri, 08 May 2026 20:25:55 GMT  
		Size: 93.4 MB (93395206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588b8579b1413f4c64c988826188cdbc6fe6d32c7bd0508c27f75a0c15ea10d`  
		Last Modified: Fri, 08 May 2026 20:25:54 GMT  
		Size: 85.4 MB (85383486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be96bc62de706652b91aeb60a2cf3320f7ad78cf3ee98aa0b9f8b6ee68b718`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f906673b199f2bf3e9f42caaf12b57988977bec62a71a026a9368f73f9cdb`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:85fba6c514fd149e583d0aededa346b4f4ba54c0d113252b6c4e3835d00c18fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d9daefd175a44d0a20380a38ccd91cf2fb8447ebdec08131193bad80a0de0`

```dockerfile
```

-	Layers:
	-	`sha256:dac6538900655bddbe60c24cca90caa855548b292a7d6d3d07c7040b36af9b70`  
		Last Modified: Fri, 08 May 2026 20:25:49 GMT  
		Size: 7.4 MB (7443252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452fcf0be5a44dcb695c6e1797a1d579812ab9203b5e7988ece34d696572be39`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:65e4ff9868c25234f8fac64bb12df98c77b88e589f0e41d8368406b5eb70ebc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237892100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afe619394953d114e42de77e7fe7b78bbc48f1ebd09ceed8030c2e8e93361e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:48:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:48:10 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:51:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:51:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:51:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:51:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:51:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380ed992dc2e5079fc5af8b7e42121e0c356119cf7446f3b8707b481cc61b56`  
		Last Modified: Sat, 09 May 2026 02:49:19 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab54cd1bfb23e902111f600dc118cbd453e9ef166687d593e5b949e7cd4115a`  
		Last Modified: Sat, 09 May 2026 02:52:10 GMT  
		Size: 91.0 MB (90986441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7b9087636cb5e789fd74cb23e8ea79d7c530111ee4f152a1f53931a566fbe`  
		Last Modified: Sat, 09 May 2026 02:52:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4205249714161c6bc7abd6d5c9ab929597078daff4e16586ec7000412734fb61`  
		Last Modified: Sat, 09 May 2026 02:52:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b3dadab7ddecc8f22831ddb22a9cbf8c7c71e44791d636ef294b4f3e7cb389c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502e209c60c5974fc4d0996aa84c3bb56af2c0a437062333d793103cc1de340d`

```dockerfile
```

-	Layers:
	-	`sha256:4e47470ebab6f71c847423bcc62b9380a66ad42064d156264c02a0551a56d2e7`  
		Last Modified: Sat, 09 May 2026 02:52:08 GMT  
		Size: 7.4 MB (7424582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb475853c0d316b2d966d1f00270753e16ac99e353543ba6080b6980c8317be8`  
		Last Modified: Sat, 09 May 2026 02:52:08 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e92089c8b7d633f22a3dc377adf8df0d1e492ca54899b9bc1ba3ad95ebe5c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225267388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a1754edd8d35002a241aeea9adae916220f248f738f59b69410a4c4b177908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 16:01:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 16:01:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 11 May 2026 16:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 16:01:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 11 May 2026 16:01:03 GMT
WORKDIR /tmp
# Mon, 11 May 2026 16:15:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 11 May 2026 16:15:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 11 May 2026 16:15:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 11 May 2026 16:15:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 11 May 2026 16:15:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16def90c932096937daf06d99b8e59a8b74b84aeebf2940aac17817b2f543a80`  
		Last Modified: Fri, 08 May 2026 20:37:07 GMT  
		Size: 47.8 MB (47798394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0f4acc8cec956552b1a476260bd88efbe51fd2f57a9fc72473564766b8edc4`  
		Last Modified: Mon, 11 May 2026 16:06:45 GMT  
		Size: 93.0 MB (93008125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a81e5c64902cc724be8316d2e2bf9d1cf587196f25c31d3d019f2cb9d1ed036`  
		Last Modified: Mon, 11 May 2026 16:20:10 GMT  
		Size: 84.5 MB (84459825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06604471d8a4d4bee7f10589c1b8c7c3c0799afcfae75ad633798b087346a929`  
		Last Modified: Mon, 11 May 2026 16:19:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a1038680126e1bbbb1dcd684edf5245dc24f94e8879b71773943cf198476d1`  
		Last Modified: Mon, 11 May 2026 16:19:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71c67ab7e92c887cf1fd8c1458c5d03403996bc9d6c83c0be64fa5bd8013fa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5320163f6a2fdf428e29044e6bf5b79ae6c8aff5fc623b7ded724ead29657fd6`

```dockerfile
```

-	Layers:
	-	`sha256:a4266432fd6c165ff08900d401871b4821e367b1144ed932b8fc6458e47b4884`  
		Last Modified: Mon, 11 May 2026 16:19:59 GMT  
		Size: 7.4 MB (7406775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0ff4ed3d6e16b35572b026d6cb82ff7251e29761b3dc410ae9eb0d1f8ab4c05`  
		Last Modified: Mon, 11 May 2026 16:19:57 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:047a2829370e23164ac2d74e2c518903d8f4dc87c68b1d00a1c7851674538617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226466462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d120b4fc5a6beacad016c2fd013d4a4e37ea2d65257b52747bac186e2d121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:21:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:22:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:22:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:22:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:22:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:22:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea63852b62fa38d78ab507e59ec519d91cb7d1e9a5a2d2372b05f64d7765244`  
		Last Modified: Fri, 08 May 2026 22:22:06 GMT  
		Size: 90.5 MB (90547732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29115b9d465169743fb26c34f2703f3cc2abc14113553aa142a9842774e96a78`  
		Last Modified: Fri, 08 May 2026 22:23:07 GMT  
		Size: 86.5 MB (86545389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de4afb669dd353b971eec2751079b9922d002695c2cb4ac5063b88ed33461e`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b456f036b909a386dbeb978f84f0e5a5040fdfde0a1b088e8f18ef144c6ae`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:133db1d5cf53849aa1180d49ddb43267b04ed0caf7524843c8b493a3204cabca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d2d3828ad872b4bbca8a29cb92701f6b9d63c307a4f0e75d7f9152d63ce4d`

```dockerfile
```

-	Layers:
	-	`sha256:65766c7a4104d477f3198ed3cccfdf2869197297e56de4750ca2987158334fed`  
		Last Modified: Fri, 08 May 2026 22:23:06 GMT  
		Size: 7.4 MB (7417333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21451cd3c94e47bcebdb88da3201a35c63b104f49c01aef88135dcd6cdfd3afb`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
