## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:33e2ee0e4cf40d1182498302ca70a8983d8bf33d6df0f12c36fbb8f45a2e330f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57ba3f807088e18dc7bc766cd3b2c469ebdc1c0c433c2f9e85500f69fcd89cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267800561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c57ae8b1f21d345e6bd83a91730525c0dad7589b223d10a155371e8d243bc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df56ff48c11fcb7b8faa42206871563e9e825c664b51ad4342fcb70420d672e`  
		Last Modified: Tue, 01 Jul 2025 02:39:37 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5392eff9247a1cd51018a57735a3fe0894aabfca08147f3b1cb1d838c5fed181`  
		Last Modified: Tue, 01 Jul 2025 02:39:56 GMT  
		Size: 69.4 MB (69409674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c163ecea565fc5eb2bcfb78f9f14cc6b41e1957bac0af0085e44d13f1e432ffd`  
		Last Modified: Tue, 01 Jul 2025 02:39:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63209d87677c10c14c0e00ccc6f20b2ffe0de0fbc39cbdb2a02bce284168d203`  
		Last Modified: Tue, 01 Jul 2025 02:39:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:342a2c71e7b08a56e93241c5248b2f41e6f7ad4befbee958e0831e78f65662a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b4d3a5ba044ceb067c60c5e504e9284ae4e2e8e26164ba16a6880fdb399e9`

```dockerfile
```

-	Layers:
	-	`sha256:8c277b782cbfb43ab4b4972d5ef4d3918e8d53fe57f4979f6de36ccfcf3ea775`  
		Last Modified: Tue, 01 Jul 2025 06:37:04 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7626d1df349cc4b3394d0d7db3921faa7f8109f9f935449ff802caf3acc32e13`  
		Last Modified: Tue, 01 Jul 2025 06:37:05 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be410ec3591d2fe449dce8495ff28c1e7dd2a20fadc0d884e20a925a8357be29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265303819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1c0df0fa2011ae8735a03f7578f76dfbd13cebd127b44826ea56656460b1cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52047471231147f9324f60740043bab699411c5c3327c1c1cef32a01098f2e`  
		Last Modified: Thu, 12 Jun 2025 06:50:49 GMT  
		Size: 143.5 MB (143512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62030fda41c00357d55662919f6b5920a4a18423d364ed2d835d2314971699`  
		Last Modified: Wed, 11 Jun 2025 08:31:11 GMT  
		Size: 69.5 MB (69537835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eddfda3f5311c2d8bfabd99409612fdd5481b41b52206b8dbb858ae04fd5dc`  
		Last Modified: Wed, 11 Jun 2025 08:31:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caac6a3714dcf1195800b731b91cb07ac5565562425ca92996ddfede25ab370b`  
		Last Modified: Wed, 11 Jun 2025 08:31:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7bfe3d9dde9036de80cd379f00bcfe140fe572b97a9ea7b9a40d84cb6517d739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eed884ed983af241600737da1c4f09092d70a2b9d197ef195b18b883397b8b0`

```dockerfile
```

-	Layers:
	-	`sha256:dd958d174a36707d15790a8e199fe1dc81947b270ed94b496e28d40b88acaa26`  
		Last Modified: Wed, 11 Jun 2025 09:37:31 GMT  
		Size: 7.4 MB (7400737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d580580f54f28993821c3c1be164f15df2503361f74eb24cfd68c64ba52924`  
		Last Modified: Wed, 11 Jun 2025 09:37:32 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
