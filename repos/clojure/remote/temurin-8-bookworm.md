## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:151a7cf0ed33caac2ec92d734442bd5a9ae7da65bccb5d37a853bd767131f361
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:658e9547bda3684319580592ada3b894d6c4194e6560b2dbce6b58a2b6a2bacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184836831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee383de92df2f969dc61382be9af65e109c04cd183697f991ec32071b721391`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:55:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4710d118af4412b472f4838396aea82f66232586f0d0658879f878730973b6ad`  
		Last Modified: Tue, 17 Mar 2026 02:55:55 GMT  
		Size: 55.2 MB (55170164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea97b470bf1ae9f38cf0cf2f8e31b46f4e69aa525f928705829083b7f5542bc`  
		Last Modified: Tue, 17 Mar 2026 02:56:33 GMT  
		Size: 81.2 MB (81177440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabeda67eab2cb487136a4f5dcc1bf34adf56ce72203365e2418f94cbf15d399`  
		Last Modified: Tue, 17 Mar 2026 02:56:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:da71084fc7c9535ea5ffe8e8e503817faaa6e0447205eb5824eac8b65a2f79bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11032f2d5a56c5f896df7bf7eb69090195f2d85ede4707f273840ad8adb394e`

```dockerfile
```

-	Layers:
	-	`sha256:26fcf3cc10687c6debad2c9c0f79e574ff1d5db3339daba1aafa931078d8b005`  
		Last Modified: Tue, 17 Mar 2026 02:56:32 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5588f81c1f76187013da7e5ee605cf413ad105b827771f2975d6038993e43a`  
		Last Modified: Tue, 17 Mar 2026 02:56:31 GMT  
		Size: 13.4 KB (13393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7df449cc7c0e9a5faaccca7416c9222fce4b03f120b952205bf3559752f8df43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183783525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5991d72586cd1323c178199004b68ad0890957086d9b7ac02b30db9b81655b50`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a513b8bce7f7cf26166b321b9e5cb84d65c8b71de289d567e537933ca7b96d8f`  
		Last Modified: Tue, 17 Mar 2026 03:00:06 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92216d764e2b2eba8457e131c3f61e001499e1a621cf7987c87ab5f0e32ad2de`  
		Last Modified: Tue, 17 Mar 2026 03:01:05 GMT  
		Size: 81.2 MB (81158238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f2e1ac525697c66bd86067fde452fd7f8607de423fb3936165c4564d10f662`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:db01a2891e4ff2e29cdf8b5d026ee420f6787ebad52d0e4835362a4d4074591c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b42461249f7f3dd5e5ddc44c45c2b0f99d91f49f3e18a17d7b020792cfd27a`

```dockerfile
```

-	Layers:
	-	`sha256:36b957b8e24acab36474e5378ba56d1b21bb9dbc2d20f7f75721bfb6b5bb43ea`  
		Last Modified: Tue, 17 Mar 2026 03:01:04 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cfebcd8e33e9672d4e02384fc9d7d81b466f4300abd0447bdd66d761f3d9c6e`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 13.5 KB (13511 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:55ac0e27f0f338ba03862a774c90bae75c3712af509ff0ffa8491382c83cc988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191988102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fba79ed7825bcfe3e11010ec2ae20459a721bf9ae2113b53317f7ae1b38e1a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:39:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:39:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:39:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:39:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:39:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:40:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:40:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:40:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddabea4c3e699b365e41713b79393b33de3ce0510481047d09732b97ab7d543`  
		Last Modified: Mon, 09 Mar 2026 20:41:22 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd804e5aa0805ebadb14f7f878f28612942b9af09cf4117281c20d99eb348a`  
		Last Modified: Mon, 09 Mar 2026 20:41:22 GMT  
		Size: 87.0 MB (87000270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2364a1a4d2ed38b827c3ab5d4293987b24528dadc8838c410860b5eca04e02`  
		Last Modified: Mon, 09 Mar 2026 20:41:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:581270301f85db8ec83c30aa71cfa6411f0872226d9da896e35c77c49c6a06a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ea56b368f48fd7f125aaf70d700aecdc8d7348c11371452846b68bb00b2a40`

```dockerfile
```

-	Layers:
	-	`sha256:5193d6fd705b6e5a082858fad959f4b56bf4725d77b633881947c00880f92f98`  
		Last Modified: Mon, 09 Mar 2026 20:41:19 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca400a106d07fd1e2ad0a419d53153dce308ae4982dbe9239be2b8ec35817848`  
		Last Modified: Mon, 09 Mar 2026 20:41:19 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
