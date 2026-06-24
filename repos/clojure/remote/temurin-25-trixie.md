## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:961aa459e9946aa80fc6b2947b4f3b98805bcc71969deda8da1d66793a7fa44b
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f1ac21b3b4903844673bbc8a6e3342b13ecc2cb82c6aeb819f91167a16d1f207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224412220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28650c08f3a4fd601d743ca089e287a0632978f2201a961dd49250d48aa29752`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:03 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:22:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:22:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce126eb699f14f9a1f39b96f6c8a862905b3bbf65aeaba02b8897551b5056d60`  
		Last Modified: Wed, 24 Jun 2026 02:22:47 GMT  
		Size: 92.6 MB (92574611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df0fec052e4f2e47c909b1fd660e435b5a304c6ea72c13689c49c28534ddc12`  
		Last Modified: Wed, 24 Jun 2026 02:22:46 GMT  
		Size: 82.5 MB (82519314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5a343cbf248c164fa7347eb48ef2811f0e5e9464c888fb69eee9603a8aa2ed`  
		Last Modified: Wed, 24 Jun 2026 02:22:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75736e7b67bb4b249842d241ecd7a1da21ea13936718b317b78bda5b29ede8f1`  
		Last Modified: Wed, 24 Jun 2026 02:22:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b8be780fbbbb44bcf5ff094e46b016270f6873a55155a1907ec7ebe673dbbc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3e92855caf7a1dcca4cbae63d25d85961aa004a54a88dfbcd79bbe77ab82cd`

```dockerfile
```

-	Layers:
	-	`sha256:f2898ef9293cb075aa7cdc0f00375b73329a92dea497a920203ddc2531c958b8`  
		Last Modified: Wed, 24 Jun 2026 02:22:43 GMT  
		Size: 7.4 MB (7436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63150d21ee67df437be98322caed2349774efe788b6b93f323520b425a336746`  
		Last Modified: Wed, 24 Jun 2026 02:22:43 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9bbaff6ba00a002db898262b801e42c37c3061c621358f09f82d144eb8f869a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223560132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75a16c826e55dd599ca90ed0768b4ae8855ea5760f7b71a0bbc177e58cd807b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:28:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:28:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:28:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:28:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:28:39 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:28:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c5874a8969a26a7ef7265fc10b9748a43afa950aa48ee602016c610720668`  
		Last Modified: Wed, 24 Jun 2026 02:29:22 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879d6e215bd86652915b84c018438fa54f125756104d8a213cf33cbe2332ead3`  
		Last Modified: Wed, 24 Jun 2026 02:29:21 GMT  
		Size: 82.3 MB (82338428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc6b08e9379a7ecae55958289ca3acdfbbfd0543eeb6f692ab59fed75a3ae4d`  
		Last Modified: Wed, 24 Jun 2026 02:29:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da4354bf17b7f8ab22aa0cba3ec247d34b2e0f5e834a9626374cc80a97e7ea0`  
		Last Modified: Wed, 24 Jun 2026 02:29:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:14edaa0a37178199ba7e6fbbf889067da9c28801f50dde6447c0ee8aef5ae294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9050c442fc9885f92bd160cf983d3371fc2045feee04b17a3153962eaa86012d`

```dockerfile
```

-	Layers:
	-	`sha256:7e2da304f70fc2d94f3e19870429ab40c24c8c49c5369805aaf1284ca9ac7650`  
		Last Modified: Wed, 24 Jun 2026 02:29:17 GMT  
		Size: 7.4 MB (7443247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67724fb4f11aebe13b8bd9a28d379e29e05bc5575fffc2ed46f114dc6de93c2`  
		Last Modified: Wed, 24 Jun 2026 02:29:16 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a14f7df036b0198bbe388c169872056e2f4880fa560cf22a9266fa619004658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232991702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbac9d785fc2700a65240c72cf90d6a21b18603dde6cd733b0c9ddbddee2e8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:22:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:22:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:22:48 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:22:48 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:29:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:29:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:29:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:29:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:29:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569624c84d9fe15712a7dc55be5d215374ba19c853dbbee2b899d5f34400f10`  
		Last Modified: Wed, 24 Jun 2026 08:26:03 GMT  
		Size: 91.9 MB (91914013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387b70cc8be3d9338457c46e09952a78f65bb5840953eb05f368882c71dd88b4`  
		Last Modified: Wed, 24 Jun 2026 08:30:36 GMT  
		Size: 87.9 MB (87938577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126478901b3ec5b40b2cf218e89b8de9c7a993b54d5e25aadc348e392a7836d`  
		Last Modified: Wed, 24 Jun 2026 08:30:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff93ad74a359c2ded4b9fec7391c94c5a93601883594e1e2d91eee7bb821854`  
		Last Modified: Wed, 24 Jun 2026 08:30:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:711cb11566af46d88c6628ceb7344f8e3dffed7ff5675dbdc4c3f8a737651840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feba7b9fe2d7ab63b7dea9bbd2b46fc0d36cac2d6f3b61b93143fd3ea2da9ff`

```dockerfile
```

-	Layers:
	-	`sha256:e6760865559be4d73ffbd924f122e74e0b63ba7bee24beebac908518fba8104d`  
		Last Modified: Wed, 24 Jun 2026 08:30:34 GMT  
		Size: 7.4 MB (7424578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90db82a5bfc8faa812efa25ce50863c432f87810669754c45ae29c4eb387e76f`  
		Last Modified: Wed, 24 Jun 2026 08:30:34 GMT  
		Size: 16.6 KB (16629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:63b4f48ce43848f092ad693e53de0e82b977b0668751fa0eac77c4a622bf99ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221309522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69962454054750803916ed2741629c573de4076a862cc2b4b01549d4d32167b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:19:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:19:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:19:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:19:18 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:19:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:19:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:19:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:19:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:19:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b31fd13e0701e521e8c62879dc7f324176cb4b604a2504e85f44c3997c0f215`  
		Last Modified: Wed, 24 Jun 2026 04:20:03 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d83c908d1d8aa60d7d3ab888bc8034a74e3eb11c307a9e53366c740f3c62457`  
		Last Modified: Wed, 24 Jun 2026 04:20:04 GMT  
		Size: 83.5 MB (83502082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5597967e81bc3f3218cda0097e032efc05be7fac485420fe1dd4070589d6b3f0`  
		Last Modified: Wed, 24 Jun 2026 04:20:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c436d65dbb20116dd1c6d65b102fea0df4ec3266527a4f2ec01ebf54ef8f0`  
		Last Modified: Wed, 24 Jun 2026 04:20:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:665d2b71d9858034e8284a06b54e785e0bda44e93597f057924cfe8c5a33c8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dd320bfca13b436b1aea30631ad54b5caefbf8c84f8543fb3579d6074a717f`

```dockerfile
```

-	Layers:
	-	`sha256:37fab07586171868c5eacbdfaa2f91b0f6a58d6a890591997833aa7620334af1`  
		Last Modified: Wed, 24 Jun 2026 04:20:01 GMT  
		Size: 7.4 MB (7417317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87dc371cb5ee4cbccbc117426dca022e2df4f90737b7d3eb92a7b1babfeef38`  
		Last Modified: Wed, 24 Jun 2026 04:20:01 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
