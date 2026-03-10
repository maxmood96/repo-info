## `clojure:temurin-21-tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:9d6005fade69900071d7704289f2f2e268a248c943b592ec2535753048fb1eb5
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

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:59417e5a1bddd126bde031fef3c132e576d78743293b2234786ebdaa368fc6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287524454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e2471bc659ef179e28dea19af3b8cbe5e1d5c4711b28fe6edcb7f9c581109`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:35:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:38 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c500957a900b1dbcfb15cc9f25af4115366236e5fcc818bc7f88ec2919dfdeb`  
		Last Modified: Mon, 09 Mar 2026 20:36:18 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354e3b995fa112872a7523eacd58dbcd3f3fb1c61f812888cce267c0e7486ab5`  
		Last Modified: Mon, 09 Mar 2026 20:36:16 GMT  
		Size: 81.2 MB (81177553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3accb38e79daa3fd9257e111a16fba63e66719704725c72658b0a4fee6545b64`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5ce9c7299b5f38038fd9996da4295625a29667d245851e84c0022a62ff754f`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:985cad805c12757d0dc05eff61aa16c5bd563aa173592db47a6c3c74a6fdc1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169572fdfb6def5d7b34ad9ae3b6b79499ded64f114503764946a4419d6e1502`

```dockerfile
```

-	Layers:
	-	`sha256:d345e75d6887b323ad791974a93fc8bb180a0886342ee58293fae65ecb455756`  
		Last Modified: Mon, 09 Mar 2026 20:36:14 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15159e5152592c6e7239e5ffdde12c5a1b71d88cab33ab900abd2181c4f9245`  
		Last Modified: Mon, 09 Mar 2026 20:36:13 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e83c68b8cacc57363748db98d2b858db4079a91212824ab73a648efb45d52457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285665559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0951181453e0a193f3c385a47f9e60c36cb8b6cdc3a451c13a931e75a650932`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:35:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:39 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de174c3d6a5cc498db287d3095d7afe7c82ffaabd3311969f42947a548be39c8`  
		Last Modified: Mon, 09 Mar 2026 20:36:19 GMT  
		Size: 156.1 MB (156133007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d68bef848de4c581829830d84177450b970f9c5230d258926587f5d48940c19`  
		Last Modified: Mon, 09 Mar 2026 20:36:18 GMT  
		Size: 81.2 MB (81158299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52269ca9fbb50a5e6199dd87bd74874b308c545a3a1917e0e5fd0df4dd1fa18`  
		Last Modified: Mon, 09 Mar 2026 20:36:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a352d0cf432a92ba347cb5ee6777bcb8c3a7d560d1e427c516f8bbc48afcd0dd`  
		Last Modified: Mon, 09 Mar 2026 20:36:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:eae82282fccd97a179fe9b426cb7981682e3c6240e75e814d58966c1afd872ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3d0d397733d9fc885e141e0291ce97b6e083a175a04534fd1d3842b3eb3ba9`

```dockerfile
```

-	Layers:
	-	`sha256:c455f154e764a7ce09a5574dc684c6527adbdab1712b5b827ab4e475527c0248`  
		Last Modified: Mon, 09 Mar 2026 20:36:15 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625c48cebdbe0133f22870100d593e8b37b77cf73780302bbd5941b35e2897c2`  
		Last Modified: Mon, 09 Mar 2026 20:36:15 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:e5770c1197675761e6b779e9122c9fbc7c77de498304ccbcc61833b7e5d9244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297315597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33c11e7d85c60ad6f7d46da29597690aafab75d01917bdb2b3a43a755dcdb3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:57:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:57:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:57:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:57:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:58:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:58:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:58:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:58:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:58:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa55a66ef4e8dff32d0371fd3807d5854e51d4a75ac606239492131837d03381`  
		Last Modified: Mon, 09 Mar 2026 20:59:47 GMT  
		Size: 158.0 MB (157977536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac930b650181bc323783cddf5508c88741a644bddf638c409284f9839621f0`  
		Last Modified: Mon, 09 Mar 2026 20:59:45 GMT  
		Size: 87.0 MB (87000222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3664d8f6e485b2ed7c7f05c7935594805f186b674c0fef2339157b2fd4c0d44`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a414f10948b4dd5a581827c41bd82ddfa0b23d8dfbead9546e4e448c9ef2a00e`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:0944f56db65087474d372d341a37b350353254406b853f359a5db1d95e699ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b33de67073feb39730c68cc0637f025c4e492daf8e04459874aa13db8dc00ab`

```dockerfile
```

-	Layers:
	-	`sha256:09762b62ae99b5f8ce95681b9cb7bc0e455a9f5d51f24990bf1f71550d10e8f0`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d9c282558e075a4300746477ac118dbe930e5e6fb5e1a8f22670201614d46a`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:f21cc8c30ab3ff044cc3a9a69bf23f796f2344f99132cb45f7b518bd5c3caca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274242529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c833e1a5b95260d88daf7d4defdca06667e3af2cc103a44cf9a33f68a85fb5e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:36 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:49 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29ec04601a2a589bc0be8cc472ba2db423eca5aa876d5b2f8ec23db6e24f491`  
		Last Modified: Mon, 09 Mar 2026 20:36:23 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79775776059699fb1f5919f326e973850cb556e4713c4229656e46c0930e05ac`  
		Last Modified: Mon, 09 Mar 2026 20:36:21 GMT  
		Size: 80.0 MB (79988092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7235a3899ecdb838646db098e266c82fbfb8f1f77a769cd53f56fb9bb35235e2`  
		Last Modified: Mon, 09 Mar 2026 20:36:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc22db24a817b24b9d8c2241f648c9319910fafa5a55f395fb2c77480e6ef8`  
		Last Modified: Mon, 09 Mar 2026 20:36:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:cd63b26e4018d0f48182009671c741a85b8c89a845c8746b8660ed6817be5613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdacbeb1c665804891a1b4c4ea57025de835969956a232def0939632828d9691`

```dockerfile
```

-	Layers:
	-	`sha256:6644a7efb5c226730deea54bee1d954a83d552cfd70ee95e176617753edec1f6`  
		Last Modified: Mon, 09 Mar 2026 20:36:19 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12483353ce56e01c07b1229a3f793beaa82aa5db035918ed12bf60ac214bc05`  
		Last Modified: Mon, 09 Mar 2026 20:36:19 GMT  
		Size: 16.5 KB (16460 bytes)  
		MIME: application/vnd.in-toto+json
