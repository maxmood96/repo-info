## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:c263e0109aec08c8011f45ef744720738a60bed18db35199153ffc434b865642
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6308d06b796bc76c9c35904ca43dec5f4e104dc974bc9dec91494dcec22ea147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292617954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7431a20f64e34a9afc4ec2df2849e81d99e87eca3dd8ccafcae1efbd7697628a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b9a6259b1a3d674d122cf697a74d83d9cb804b12ede8d9bb1b1913d132d5a4`  
		Last Modified: Tue, 23 Sep 2025 12:14:58 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664667d9104f33cd69bf83779145b23ddd93f2e3207717654667815f0e4daed4`  
		Last Modified: Mon, 22 Sep 2025 23:47:02 GMT  
		Size: 85.5 MB (85532603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f8d79a3b7e0011c17b708d806eab6e7c059d9ef27a82e17d218328e34c5f99`  
		Last Modified: Mon, 22 Sep 2025 23:46:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6308d8c4204624c0c8bcf0b059a2add15cb008a98e1ef170eac96bec0810b769`  
		Last Modified: Mon, 22 Sep 2025 23:46:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f47bbe4b25b6d540ff4cab0a687f00acc64bf37f1d36797a6bec12f33337d99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92271ee6a01cdb895ecb28a8372da6ee1fb2ffe4f768ee3b9c681ac73506c05e`

```dockerfile
```

-	Layers:
	-	`sha256:309ff092141dfaa82c0e372face59bd4298d17025a6624b7213bf0165d244efa`  
		Last Modified: Tue, 23 Sep 2025 00:42:45 GMT  
		Size: 7.5 MB (7470615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd92c9910326534c9e1d038aa26af8df9cb247dec89c0d9807e52a206f87c567`  
		Last Modified: Tue, 23 Sep 2025 00:42:46 GMT  
		Size: 16.5 KB (16464 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9bfab3e1092228797ba881ff2f920940597aedd98f88dbdb2983d0b8ffd2e43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291083856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e361e904b72f81b9303f775d6350080bc4b2afe4506a8bbacbb57528ce5e5a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae115bf635a3931238ce92d5621196600eac87d74915e88a5bab0b35fea3e41a`  
		Last Modified: Mon, 22 Sep 2025 22:20:15 GMT  
		Size: 156.1 MB (156081195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b266b89e3bbadb1ab80320a4776b81dcfb9cbdc6a353d3b8bf5e08b4999cc`  
		Last Modified: Mon, 22 Sep 2025 22:20:27 GMT  
		Size: 85.4 MB (85357873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39da6aa3aa61f33b0710ae8b5f5a4e2793d45044d63a142be9e6dc5afad0ce7c`  
		Last Modified: Mon, 22 Sep 2025 22:20:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d17615cb83e24d0a6bee61938350097e6015debdcc963df698ce2df543c4337`  
		Last Modified: Mon, 22 Sep 2025 22:20:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b964851ee8a7292e44ee90b44b99a6848d78f5eb42d80030abcb14e3e689ce1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550624d02d5abfa13955990669503d4d4d84a60a46e9d9042499bbe4ce8d653`

```dockerfile
```

-	Layers:
	-	`sha256:1623175016c7bc8ec014119ef03a72770644a03b103132e4d7e5def2ca4f0f8f`  
		Last Modified: Tue, 23 Sep 2025 00:42:51 GMT  
		Size: 7.5 MB (7477669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33a50684bde81aa753d2a597ceb39a24885cb27dcad6fb399c086177b88e9c7`  
		Last Modified: Tue, 23 Sep 2025 00:42:52 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc0e9cdb00210cf4ae8e435ea703ca22e0c868317e6d46f2f5091999d0cbbe9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302022976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee626851f72aabcd7a571cb553e89617b0f00518520b224d263e2ad6b707189`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a0fe600fc915183c026172674fb5e7280f1bd643785733174c9a336a264db1`  
		Last Modified: Sat, 13 Sep 2025 03:46:18 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40252c3226d2b90f6632fe84607de472bbce06f0d2ed84f829dfa2a253c440a1`  
		Last Modified: Mon, 22 Sep 2025 23:18:20 GMT  
		Size: 91.0 MB (90954029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdd5abd327074dbd45340718a66bfd71d3d55e426f85f00826c26df8c515056`  
		Last Modified: Mon, 22 Sep 2025 23:18:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4c5606f0df862e8478af5d05afca33db89a1c9a994f715d6df99d3131ed015`  
		Last Modified: Mon, 22 Sep 2025 23:18:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1f3a3eb711d632d63289dbb182dfb198e5e57f441b1ba6bfaddda0bcb58da9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12802f446838ae6e34940bd4ff334a70f04f40c9bd50fd0cecad6f599c290d87`

```dockerfile
```

-	Layers:
	-	`sha256:21059027778350759c346c8d82a3f23d468d7e6648ff514b24bd5acbe5eadb78`  
		Last Modified: Tue, 23 Sep 2025 00:43:27 GMT  
		Size: 7.5 MB (7475046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826d45b63873ad53a61a5aa0cad6ad29ecdd36132dc2032210b4f6d777be2f3c`  
		Last Modified: Tue, 23 Sep 2025 00:43:28 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:10b95a183325ed4bd04a57c638565611633d83c02661cac5f97a4d18b1ba29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285788102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa011b98ccadb06c6f9496b366baf156e2912501b5a8f1dd9688f0c6a1e83da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d16d1a64bf63ce2a46fd192fcc03ef4725134c5c609d93baa2aa37b68e7d97`  
		Last Modified: Sun, 14 Sep 2025 03:36:09 GMT  
		Size: 153.6 MB (153593506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db6ab702f033e45c4d18d4cf9ce24d2626251027a8bbce422e915e5e22b477`  
		Last Modified: Tue, 23 Sep 2025 00:52:15 GMT  
		Size: 84.4 MB (84428102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a3da70f43611d1efc4a9f742977f7186d18e164404703b528bdae94b39c524`  
		Last Modified: Tue, 23 Sep 2025 00:52:10 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e626fe2ca3f57a68ab8478143c485b78f2034c67ad22175ec1258cce53ea1507`  
		Last Modified: Tue, 23 Sep 2025 00:52:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:336efba74b97b2e442729b66008734ec91e7bf9a19879a08334cf15383facbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8d6e655449e3b33c3725e73a6369e73d91fe9f090e8df208f274a185d2aa3a`

```dockerfile
```

-	Layers:
	-	`sha256:da5a879d632522f40c79440c9d03e3c4ce94b75ed06c9d2ca011f0a3f7ff146b`  
		Last Modified: Tue, 23 Sep 2025 03:36:50 GMT  
		Size: 7.5 MB (7458540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc6f3adb578ba47fcfb1c76426a65fd0d240355facaf1e18b6f3dcc7c83eab3`  
		Last Modified: Tue, 23 Sep 2025 03:36:50 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e209c8a07f38c64840bb49f3b2e21f2e989deab88a8a922fb544f5a99f7cca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282883310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6921382f178de2d36429fe96f4c365aee5a0c442bead1cf795d2d6c726fd75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00875a6a6fc9f065f3a5f8832c3ee5703ed6039afcd98d63f4d710eeba4cd65`  
		Last Modified: Fri, 12 Sep 2025 23:58:41 GMT  
		Size: 147.0 MB (147027042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a541bf157cd2b7eee86d3c251715ee008c12816ae665c22de20e749a03b3b53`  
		Last Modified: Mon, 22 Sep 2025 23:17:10 GMT  
		Size: 86.5 MB (86508899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe34b92d3d08879d3fd1bbaa5f110a4fb3457555b1b13fa805cdbc485fffc89b`  
		Last Modified: Mon, 22 Sep 2025 23:16:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97753fc1cc06abd1c2e03f0a0bb847cbfcf40b8cc094d639b89e5c729554540`  
		Last Modified: Mon, 22 Sep 2025 23:16:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2980364074c86b292afb04806a2c83a1f9e4aaa2c8f8ef84bf3fa74ebdb51b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4754cc8395bf183948327f79bfc5af1bf9cafd0e74e63d12dfeceb687108bcb2`

```dockerfile
```

-	Layers:
	-	`sha256:722f211e14844ab6081219400432c683a1d5c88bc2e644547df65657c51f6c9c`  
		Last Modified: Tue, 23 Sep 2025 00:43:41 GMT  
		Size: 7.5 MB (7466537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3ef3ab7a3d6cc1b4ed1509de1784cb9cdaa1b6cea462502178344daaab72ca`  
		Last Modified: Tue, 23 Sep 2025 00:43:41 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json
