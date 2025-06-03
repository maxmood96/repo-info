## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:6c5d64a6d35d348ad0c155d49173c985bf5d79f5875ed539b92550d410f66938
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

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:aa8743b2ef850539866565c4a046e0c8e5f80f0e284fc9b508d754a581cd2078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287118530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62d63c8f6f2180774db8da130a939597b34db376bf969887a132f24b5bbb216`
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
	-	`sha256:320753fd20777ee40e9178f35d9debcb6e06f4d9b16468ae9463d0d4cb84919f`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 157.6 MB (157634484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda9780b5dcaad7e90c7d0dc1861000ba42fd8f0d9e613cf335885aecde4a74`  
		Last Modified: Tue, 03 Jun 2025 13:33:35 GMT  
		Size: 81.0 MB (80994763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8b719f8ec5f897a6a544c34ca08adb8268bf1d32c2319fbbbb613e74acbbb2`  
		Last Modified: Tue, 03 Jun 2025 13:33:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036a55dafd31ccc2a0c4a4a09b3f5d9dae8fb84741a9a01f76c925b0d25777f7`  
		Last Modified: Tue, 03 Jun 2025 13:33:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:0827f6e1323f2fa7b5d37ee54e3686e94fcab4c7349edddf98567f6600eaa022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78c5f2d8a8999bff261919e4f981c063311afefb3b985674ed75e2f1379e765`

```dockerfile
```

-	Layers:
	-	`sha256:d380a9a4708c293a45f9e2de13aca76be4bd645e3b681ded7ad5e85d1e7677e3`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 7.2 MB (7223624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f222828fc20a17df78fa93f12d0c1b90b0f3c8c7c451a97214597004ba0efe`  
		Last Modified: Tue, 03 Jun 2025 05:16:31 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7bf9eae569250ec437eb190d510e67a5108025e0c9e2b382345bc434cec112d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285103764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22071bb7f981aefe025ba9af927a4d6b901c1a26e29305a32d86ad60fa66a602`
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
	-	`sha256:437f8f7a50b2952398084c7b3ca28b3cfe6e72e05419b0e1b568927135d80a2d`  
		Last Modified: Tue, 03 Jun 2025 13:43:18 GMT  
		Size: 155.9 MB (155928814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe265804159a8d38d3407e4784934106da69d6f25e551ac2d0b32de33b7789a`  
		Last Modified: Tue, 03 Jun 2025 14:17:13 GMT  
		Size: 80.8 MB (80846728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6482961ee7e1e3c5a20b25a440455d82a5d1b23498a0e2d68c57df98d752c0`  
		Last Modified: Tue, 03 Jun 2025 14:17:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fb379436ebc12d3e86625f8d53402e3be67793951bba0ed67f4c81152fd7d7`  
		Last Modified: Tue, 03 Jun 2025 14:17:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:972c55ac367956c8111dea181f7654ba58f2a5e22a2babaeb18d7b097a399aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09595e7ed9956ff5be4832d8f74b74f4eee4e629aa74db779a31785d62027b18`

```dockerfile
```

-	Layers:
	-	`sha256:4a39eb528ee94c40e6d87daa1295db17792c0787d6a5fe762d10f2a0187abc10`  
		Last Modified: Tue, 03 Jun 2025 10:58:51 GMT  
		Size: 7.2 MB (7229459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94d0dc34fa9a7ba136b128f923d370eb0008f52be8f5dbb8576b624aabe7fc3`  
		Last Modified: Tue, 03 Jun 2025 10:58:51 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:df3630d7c11dcc97d7f15a34257441bbd1bdcaddbba1540768a31a9a65474329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296948142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7ae90a5e32ae29483144b57e8c1fdc85fb34dc6e34cd0850b540d83fac2136`
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
	-	`sha256:860dcfb7182a5dc32b212ca727ac1ab0a7e7f5698fd7540ceb4c7f84c97337da`  
		Last Modified: Tue, 03 Jun 2025 08:01:20 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a448ffe1674e0e7a0ef0b89a8b8f6f27ee5aee4a19013524fe136464c0a11d7a`  
		Last Modified: Tue, 03 Jun 2025 09:15:02 GMT  
		Size: 86.8 MB (86810611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d46b72579ea7044be74b670f0cd338b523f77a624ddb480af18afc51bf396f`  
		Last Modified: Tue, 03 Jun 2025 09:14:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970fc008d58bd89d735ccca3f2fbe05191aed7c1ae6317cc19999ad07797d7f`  
		Last Modified: Tue, 03 Jun 2025 09:14:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:f99615018e3c9e6d66be0ac2b2fd75ca743356db932ac35e23f5798e655c9078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356e1023b7a619304a4d3a7a8464f8ab8837a2bed1c993f6fa5d6a501c42d4fc`

```dockerfile
```

-	Layers:
	-	`sha256:abb1f4c6156841d82e92c95d9e84fe4dcb9b5e5af1bae81fe21ef506443ee8eb`  
		Last Modified: Tue, 03 Jun 2025 09:14:59 GMT  
		Size: 7.2 MB (7228864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1fc551958dec9cfb1062f33b21a226315ab5c0bc8f82c5a7446f676587dcc2`  
		Last Modified: Tue, 03 Jun 2025 09:14:59 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:59f2995d49bbad91ae54cfec1bec827cff36c91dae366c948018168db64bf385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273845960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b679ce76e55f91bb5cb97635c99c245ddcf35063e5d24070f81c19673e1a1d5`
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
	-	`sha256:0351b5becfe334f70decb5f4368fae95fc08263ea48dd42b0157f6c4565135db`  
		Last Modified: Tue, 03 Jun 2025 05:59:18 GMT  
		Size: 146.9 MB (146911002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a539de367e49aea4e353afccdfcb7c76ca934fd96172cd4496cfe08d0212e6ff`  
		Last Modified: Tue, 03 Jun 2025 06:30:01 GMT  
		Size: 79.8 MB (79790079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65ddb9ebbae69413046d4f63bf8282fa14c6fd4c6d56eef0db41a14eca081d2`  
		Last Modified: Tue, 03 Jun 2025 06:30:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0d5f2f37c8607fff818c3224e7e6414f3c546f89fbf18dc871a80e7c14819`  
		Last Modified: Tue, 03 Jun 2025 06:30:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:e1c0a917fcdc0d219bbba3b966d7d698eeca770ae43fad2a1f5fd841e66b8f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a04fc4bddf3e15a01be667bcaf7d1cf1731420bfbff845d98cc40386768280`

```dockerfile
```

-	Layers:
	-	`sha256:11d5421c1e6d37c4e7d5087045568d5cc4c783446206b324e55db58abea0d373`  
		Last Modified: Tue, 03 Jun 2025 06:30:00 GMT  
		Size: 7.2 MB (7217835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b5bd766d10d77f7f10a451dfdcd116e38fce7d4529943bfc87d543acd9fb35`  
		Last Modified: Tue, 03 Jun 2025 06:30:00 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
