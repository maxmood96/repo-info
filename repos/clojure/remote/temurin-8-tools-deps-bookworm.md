## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:2ff28b6836af86561d208f9e85b9713b2287dbc244cae452ded364122cec95a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5db340ef48550586cb0bba8c29d598220cec3389a5f5f2e73c4cf353cc893a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184803233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f161f90ae8b5575d0ee2843aa03bc32ddc456cf83069df75fe4e05484a260159`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:17:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:17:44 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:18:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:18:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:18:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2b7653ca77896736cdf39f9886c0b00ce81bca57c62a43956a2a23eaccdc5e`  
		Last Modified: Thu, 05 Feb 2026 23:18:21 GMT  
		Size: 55.2 MB (55170165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66863a6d34ffc4521c4acb0d79211b3dae1f6b989603f30861f13448a2240253`  
		Last Modified: Thu, 05 Feb 2026 23:18:21 GMT  
		Size: 81.2 MB (81150940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4706a6fcb8884b75ed29b5b10ab8fd5262f92e05c763b425c38b7a33e95fae`  
		Last Modified: Thu, 05 Feb 2026 23:18:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:30b10089fb8a3d326abdb3d5e83dd3ca947e2267029d61157e9a49627dab4d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd21bf27679f3a3951608c289824f3b384aa24eca8b375caf0a4f0ccb6855bdd`

```dockerfile
```

-	Layers:
	-	`sha256:5215f637a67d88b628c278dace2e262a442979791b4f252d0220544a902112f1`  
		Last Modified: Thu, 05 Feb 2026 23:18:19 GMT  
		Size: 7.5 MB (7497776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e2cf7daaaeab153f150923ced7d97954238c13a0ada65106d1d3dac0606d2e`  
		Last Modified: Thu, 05 Feb 2026 23:18:18 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b8b0802d4bf61ee93b4693c3e560ee01f862baedb8c2e9cc37ff22d88c9ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183756744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6aa7ce888daf27472ed2d4ffa596ab2fdfa7ae5e0ef45ab9da9ca53c6366e8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:02:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:18 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cbf1e690ffa8bf790db6752e7145d52a63e859a1e14bc12de726a2ac012bdf`  
		Last Modified: Thu, 05 Feb 2026 23:02:54 GMT  
		Size: 54.3 MB (54251639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd251bb57a4a275ec5f2323ab9b392d65682156140d76fb097c015f5d55c03`  
		Last Modified: Thu, 05 Feb 2026 23:02:54 GMT  
		Size: 81.1 MB (81138503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36af549fcb181bc909b55710e4e894bf5329ba3522a6f9f780d38cc88e08c09c`  
		Last Modified: Thu, 05 Feb 2026 23:02:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:96681d97378e5af385d9b3c1dd21e8dd480858766d5f985ac5a04e1f4e6f5cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7518551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74222f09989cc15be9cabfd66fd83c460f5a703ac25ca3d6f53ea57e270cc07f`

```dockerfile
```

-	Layers:
	-	`sha256:5c45be709bb667f810b27753b24ba9fe3b40c898945996917a9af76a2dbe9223`  
		Last Modified: Thu, 05 Feb 2026 23:02:52 GMT  
		Size: 7.5 MB (7504239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ad0dcdc4c2ada18c7a3992b626abb740215195dcdd49ea6eb1435d92f98a1e`  
		Last Modified: Thu, 05 Feb 2026 23:02:51 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1c335c7b17774e2c787f6233dda80606bd7f17954732934378121667aa9c06c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191965445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec9c9a187d1c84db1f0ff09d3123c270e610e6c14a30555ca227e6b405a0161`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:55:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:55:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:55:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:55:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:55:43 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:03:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c85e0b853be6e0d03b2fbec5e5c7dc3f5e5b6e6f27d9574958d9f52776d65`  
		Last Modified: Thu, 05 Feb 2026 23:56:59 GMT  
		Size: 52.7 MB (52650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a2f301a831dc7cbc558f088450c2cf45b3c5f2e488ee9f6ea35709dcf89fd6`  
		Last Modified: Fri, 06 Feb 2026 00:04:05 GMT  
		Size: 87.0 MB (86987133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d705504f3e16763e7ae933471916cd0d41c2e47031f616a694a9732a7532cde`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6c83e5a581f353fe1d2ec01c1b8e95d79b03b4c5252f1a7b7bf535d672a5622b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe4611e5836c925f719b615df4bdad38ae3f462ccf588cb732c8756475619f3`

```dockerfile
```

-	Layers:
	-	`sha256:ae7d46c3f73bcd6d4232ee61648455a17ba4f2e1cd1d9983342acf355183af43`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 7.5 MB (7503587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6a091d696c4728369e7bae9c0b875ee21b12f12ef952ff7e077db3ff1c74d1`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
