## `clojure:tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:cc691b8153f7bf308918b5b78b8ea81af6934dfb3f4413530ea54f2b202e23dd
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

### `clojure:tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:35d405e2b3b6f73be3ebe96d881531b8b741e52d9ee320ecc36de9a81fb023a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222230821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6900ef3639af5b40678b616fd406bf909d230a6eabd5c1c207be1bf9c2ffc0c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:10 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1c15b9890f148130f9ce1e03b754ed14f01d21ea740bc65a14f22afb29b2`  
		Last Modified: Fri, 08 May 2026 20:19:50 GMT  
		Size: 92.6 MB (92574572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32556bc7d62d6a756307190e0a149bf5d58cd3f8d89abdc6dac3d946730d48c`  
		Last Modified: Fri, 08 May 2026 20:19:50 GMT  
		Size: 81.2 MB (81166530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88441ad6390d0700ba4073c09987b08d9ae820782313b521408e0b6691dddc7b`  
		Last Modified: Fri, 08 May 2026 20:19:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22faaf9fa5cb78b5c259521c26b129f36e65740e05dbc3e1d94d02da9cb6647`  
		Last Modified: Fri, 08 May 2026 20:19:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:1b6917d3ffbf5ec5c4914fa88277ebb90cae15b721bb8ed61fe3de23d7235dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94526d33749917e94bc22f7904259df1a722daf7135594898c4217a9f3e080bf`

```dockerfile
```

-	Layers:
	-	`sha256:3887aa28cbbb9db2628e008adf5e86832d4718c1a88463908940d60ccef3557c`  
		Last Modified: Fri, 08 May 2026 20:19:46 GMT  
		Size: 7.3 MB (7348323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4773a7f66636ae0221633ce8bafc66cfb1d20a67bd90b73ebb7366d4707db6fc`  
		Last Modified: Fri, 08 May 2026 20:19:45 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83a77e763f71d30973a60a2aae89455c778bf5eff81f7ebad57b46d8f24aaa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221090904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7d56949b009848a15c65d29a093a20a957519b3d14f6721f87a407f4758f9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:23:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:23:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:24:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:24:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30a660f28416f8a0bc17a26769597cfba0b22f143659fa1523d91c66fe223`  
		Last Modified: Fri, 08 May 2026 20:24:27 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa783917144f0d16e05843a0ff21f8fdcd4115bc0799c153333e646792d5ec`  
		Last Modified: Fri, 08 May 2026 20:24:32 GMT  
		Size: 81.2 MB (81174443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cc065b797b48ee59f91e70fb3d4aaa48eaa7a25f4fae30dce54715b1d55e43`  
		Last Modified: Fri, 08 May 2026 20:24:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189d8da385a685645de49d534be5352f80a5c352ec9c75922c327a270880c259`  
		Last Modified: Fri, 08 May 2026 20:24:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:d172c2accdfad586b68ecedcc2e8b7d225b854b294a5d9500efc932a1d477143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbf42410f66387eba7714f5eb6a91f03263062c85c0ffcb14f94d6683c6fefa`

```dockerfile
```

-	Layers:
	-	`sha256:b6f5b97191a15d6fc65f2ce051299b9dc947f4700d04b027d8613b77da8c7b9f`  
		Last Modified: Fri, 08 May 2026 20:24:30 GMT  
		Size: 7.4 MB (7354155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09bd19cf5bda516668d478d715c443502c6ead971520af9929b96a33f3d056c1`  
		Last Modified: Fri, 08 May 2026 20:24:29 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:5ca6e21ec8eaf5386f4055b9f26ff9ecec5883b62aba9a20c8b0655a16c7758d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231255934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8051b3e66edc517d1ec2345a19d190701d9750d605551a6df41387d501ea540f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:34:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:34:38 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:46:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:46:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:46:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:46:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:46:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733e476aa8595c677a7a8e78f0fbc11c82e45660c7657482695df3b0260f12`  
		Last Modified: Fri, 08 May 2026 01:36:27 GMT  
		Size: 91.9 MB (91913990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3734258ae6f0879085c33ac8bd8c005607a12fc9792e1606358bab34ac31e5e`  
		Last Modified: Fri, 08 May 2026 01:46:40 GMT  
		Size: 87.0 MB (87004167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5c45b86b42c3f76314bbb018a424f1fbef2434b8448febfdf6bcb39acf3b41`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfe34faba218d866b7acf8c6f233eaab0559ed9bd9848c600dee559c0620294`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:d1c5636d5a22349b89091fc05729b3d63b4e14f0ad2d930151b866e33409ef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac06e2488b4cf23097ca3e75ced647dd1dc288ee15341c1b831f10659ea25ba4`

```dockerfile
```

-	Layers:
	-	`sha256:58cf8027d74f46e0b63915f5a152718e38bcd5509c4a5b1020fad193b34437fd`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 7.3 MB (7336887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acf40dddc186dbf352975542f25e9ce5b8fa7cfff8da169b3410ff0767a1780`  
		Last Modified: Fri, 08 May 2026 01:46:37 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:9b11c2bd6738b98350b3d79315115c18b4fd649eda7ef375f3609111adc1a432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215549334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a017cf573e9af4ead253147411020d8c937aaef815a7f14bdf77afeec178d1bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:19:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:19:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:19:49 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:20:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:20:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:20:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:20:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ce6e09a233f668ce2ec7425c1b4b214a54a8a22360c364854e162a4bf2f3`  
		Last Modified: Fri, 08 May 2026 22:20:32 GMT  
		Size: 88.4 MB (88420319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235993aa82d8cb67c46406cbc59fdc4af07b626c1aeeae44c69f635e831a2ce4`  
		Last Modified: Fri, 08 May 2026 22:20:31 GMT  
		Size: 80.0 MB (79979949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f00d86301fdd888a8da91d14bf037c01980ce15dfc227731beee35ac2ce882`  
		Last Modified: Fri, 08 May 2026 22:20:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41213f85a475815dd28b4ea29cd8a179cfb9bffaebd54351745af4b718f04d`  
		Last Modified: Fri, 08 May 2026 22:20:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:8463a7d46b2461190abbce81208e1b53aba1222a5537276fb2354de527e973d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07073ad613b26d52748b62d1169b87ca78354f2f8965a03ec6c983a89fdac0af`

```dockerfile
```

-	Layers:
	-	`sha256:46765fa3f0ebc8f0123e253d3a328583229c4032d0512f36fcf185a0f515cce9`  
		Last Modified: Fri, 08 May 2026 22:20:29 GMT  
		Size: 7.3 MB (7324204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8b210ced58265ec218e2b829d30876ec32699e460a6bdd22362dc08acb31c5`  
		Last Modified: Fri, 08 May 2026 22:20:29 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
