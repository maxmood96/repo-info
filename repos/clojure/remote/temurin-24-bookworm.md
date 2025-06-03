## `clojure:temurin-24-bookworm`

```console
$ docker pull clojure@sha256:049f088d53e0a7ce81559d8bf1f5eadafc205bf6f19b3df02c775acad1d99005
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

### `clojure:temurin-24-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4dfde9ac48ba8a2451d5df4b552ba8e0f49c3e9a6a52beb3bf8d7159459b6ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219436132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a04e939491c5edb7b001fbbd1dba60297e395e585643f19a4c28b657da5b879`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e5b3af59d596af4bcd7dd8ea3f9776673f9f316171286956d02fc88d392ef`  
		Last Modified: Tue, 03 Jun 2025 14:02:20 GMT  
		Size: 90.0 MB (89951990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2315ba529927164feffa8fe43dd17223361db0034dc471fe1604405611dcc566`  
		Last Modified: Tue, 03 Jun 2025 14:02:21 GMT  
		Size: 81.0 MB (80994857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822145d1a701e54062f13e429b7160e9a034dff685d41314dda280f1b3fe88e4`  
		Last Modified: Tue, 03 Jun 2025 14:02:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a1078909122b67c2d4e1529e59803aff4d159d397da2b608b3ac24dd74704b`  
		Last Modified: Tue, 03 Jun 2025 14:02:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52e6000d52a73d3da575d3b3b515ce106639d0b508dfcf6ad11469705d5cdb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca773e530c7418756702864850612ce8b1220aea4c470dc7f181a985ab052d2`

```dockerfile
```

-	Layers:
	-	`sha256:96229c89a68792638bbc7ed574b3e5a72d4828f7ab6f4f1f215beeda743c2317`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 7.2 MB (7169852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69e1be3341ba946e609a3f157c448f25d1ae72e4d0626a200550502e80fff18`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9f01a670c4698e1595b164fb028158f241488704de75e784372e1f957e11490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218267280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6de189e35671f0b126b99654d0e6bc8ce4e8a1dd8305ecec7ece0e4c5c9292`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad72b0b0d87ada56df9b871909e981f1cfce883a2eef16b29952fa54093bf67`  
		Last Modified: Tue, 03 Jun 2025 11:04:46 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa856326bf4651f658ad3ab5e35c87acdbb9077f51e6cadc2ece610664e5b88e`  
		Last Modified: Tue, 03 Jun 2025 11:11:13 GMT  
		Size: 80.8 MB (80847786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c638436c51a8459bb8b8bbce340abbc89470431ac3f4ef1e0cef2e7eda9003b`  
		Last Modified: Tue, 03 Jun 2025 11:11:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a480b3a7ac1616e80dacd8cb400e7e662708ed4c97b7a722cee7beed40bb29fd`  
		Last Modified: Tue, 03 Jun 2025 11:11:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:741a989fb42342cd0c3e33a15aa40e6dbfa80c8d29400f9fca2f8510ef4fa8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16137a835c4aae65289fad0df91fbb5db485e7808cd159cf9f40838bd62f9d2`

```dockerfile
```

-	Layers:
	-	`sha256:eff46db634326490a8274b023292635ed59bace75785f173fad0996c39b48e25`  
		Last Modified: Tue, 03 Jun 2025 11:11:11 GMT  
		Size: 7.2 MB (7175636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58a619ad197d0688bfaeba2d196b51cd19532f4d127a1d8a398f4e7edac76e0`  
		Last Modified: Tue, 03 Jun 2025 11:11:10 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ffdf8ea6ca2d99f00281f5de3820e47c61326e98b2312393cf9ad7bc79ff1a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229063029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0953b5d38321c809831e6887ad2fd75eb3b64c9ade900bf62963a36900628ad3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3937d64ddc56eababfde7af2e4d4da5a1866df46d7de0bebf9c2a99e0b0cce`  
		Last Modified: Tue, 03 Jun 2025 09:24:56 GMT  
		Size: 89.9 MB (89920270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff730217cd339a28b78412c72028a1f880b36d582fc6dcd61cef177cdf5786e0`  
		Last Modified: Tue, 03 Jun 2025 09:34:22 GMT  
		Size: 86.8 MB (86810098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ead125059aa2e0a4a27f6e9ab6f8893234eb46fdf7ae019f8dc535c4ead4d`  
		Last Modified: Tue, 03 Jun 2025 09:34:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142651b9bf1a3efa475b7c7525116c39edb28ccf4befe554a71306dbe36c69a`  
		Last Modified: Tue, 03 Jun 2025 09:34:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e694e30426b110ac1ed6577b3f54fac39f2cb14d68f3f830269a93b709e05324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba4132ec16b6dba30dbe32808947db0fb532523b777f301dde98bd8be9f4b6a`

```dockerfile
```

-	Layers:
	-	`sha256:aff822f82fc3e8d1cff161b629a20ba4e57efb18105a2c0428bd3fe395c4ebab`  
		Last Modified: Tue, 03 Jun 2025 09:34:20 GMT  
		Size: 7.2 MB (7176366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a9ec88c4caec0d307ddb049d93c1c91be0d550b989e635dc90d00396095223`  
		Last Modified: Tue, 03 Jun 2025 09:34:19 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4f348ff726dcc600f571d99b272383e40c221701e115742af4aa37601ae58957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212151921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fb2e487e9a4450082e580609e6d087beb2861450e345f770c6951f510d914`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a88af61dafe611dbf396e5a57107bc7b7f88c5b3a0ba26ce314843717b096f`  
		Last Modified: Tue, 03 Jun 2025 06:35:46 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65471463aacbf0235e11ab2e00b78d6f9eaafc18c8852541183f5be17b816a94`  
		Last Modified: Tue, 03 Jun 2025 06:40:39 GMT  
		Size: 79.8 MB (79790165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602314353829f0e228f95cb0734ada432ea7b5b94d941b656b2e6eece8d8f4e7`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6193d56c0f7c88f252eaf028d00b3c97f0f888e0216b1843d1964056365dd21`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69ff5dc6c6a73a409ad9a450b6f99bcac72bab1c1023a3b8b22f530051ad4be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d100db48ddc2f7d6474da14b2e7f0ea0f2b4b0a52c8868947bb1d29faacbb8c`

```dockerfile
```

-	Layers:
	-	`sha256:0ba1b0868bb5858618c2e9829987e8c7c8d2ce1f38e4eaf6ff561d1eaf5b6ebe`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 7.2 MB (7166611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5894ec35a8c289a5c70d9cc1f5d0c76d2673143b554f6b94ee24355b4175135f`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
