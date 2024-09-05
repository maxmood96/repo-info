## `chronograf:latest`

```console
$ docker pull chronograf@sha256:77a6f5fbfbf5689044513d2cd159d1bb255e62ae4e86246e129684d3ede21426
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:e8dd6cfbc4b2a32a50054d860945501a95483ee5a8c41955b55f3609a79d9b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84242969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f5b9bf29a6554c360fafc8d026297078b604e20d6d8f485dc5e9321e553a48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385e23c0af2d3be1bcdd522ba8d1a0440717f8907aa01e5e7d59bd40fb0ee8f`  
		Last Modified: Wed, 04 Sep 2024 23:07:33 GMT  
		Size: 7.9 MB (7874759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2042a65dae0293ea6f9e20b1fb6084cff0ceba2748eee34b215d2946db38d02a`  
		Last Modified: Wed, 04 Sep 2024 23:07:34 GMT  
		Size: 47.2 MB (47217266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52375e714f6716a7d770952defd2d82d6ef521e7ec9fe1bab0caa7ed84c4a73d`  
		Last Modified: Wed, 04 Sep 2024 23:07:33 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131eaa26a51a8b8b1f7d694641e5c7af3d0306bcd2a647dca1eda6bbe8d773ca`  
		Last Modified: Wed, 04 Sep 2024 23:07:34 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e7895d0b8772d3db7dcde352ab2b0ee023e6742c2b5dbe791d27fca3ca7a8`  
		Last Modified: Wed, 04 Sep 2024 23:07:34 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:0383ecc021c8d9fd5d2716fcfe18dd088cee7a3c197885e5efab06777aab532c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3847bc6cb5a70990fbb3ad9aedf546bb88fc1d86246fa43a48d2cd1d37efd416`

```dockerfile
```

-	Layers:
	-	`sha256:92d5880b1b1caffeac7ab15bf252beaf20629f50d0a3f8effdd32aa87e7a3ae3`  
		Last Modified: Wed, 04 Sep 2024 23:07:33 GMT  
		Size: 2.7 MB (2690947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded5325a1cbc8da9de625a44ad5b9cdafc79c888a1e3b220a68e45b9c6e5933f`  
		Last Modified: Wed, 04 Sep 2024 23:07:33 GMT  
		Size: 15.9 KB (15933 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:89ec3c1d2a6a9050f602e0c06833c5c458d4b19faf529a3a411768dfdc2c1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b9801a7139290a9718f3f6bbba15dd63b1c75c10a14789236ad342f9bbeebb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f92f6aa6f4cd539d7a7c61e8e529add8f6b627175dd8a32dc555a7def56d5b8`  
		Last Modified: Thu, 05 Sep 2024 03:51:18 GMT  
		Size: 6.5 MB (6497535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f530c89297356cc2ccc65f1ff0d4d56e14e6a72921e89913eb01bd4a9d55ab35`  
		Last Modified: Thu, 05 Sep 2024 03:51:19 GMT  
		Size: 44.3 MB (44276059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5c6044223b54ecd6e4e5865a52858c4cf2321821917b7f632c6d6738dcaf21`  
		Last Modified: Thu, 05 Sep 2024 03:51:17 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d61afd847d6c86c169a2a666430a6d4e2f42ab796431f198254451e8550ae79`  
		Last Modified: Thu, 05 Sep 2024 03:51:18 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22fd7899df40377436b08a4d417f24e343dc32824025ca27a9e1a65eaaf01e`  
		Last Modified: Thu, 05 Sep 2024 03:51:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:9c2dd62025c0b6e7b0d01002434752cfeda9ecd85b9b4cb0bedf2d5f8eb9f29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e9f23a8c2b1b7a0c3a205ca3e6c266e4093ceb2ebc421dd2e76c48765e3380`

```dockerfile
```

-	Layers:
	-	`sha256:5bf4e5190a4b26267402a09a061b981e9b451bbd984697efae6b6fdcdca4e912`  
		Last Modified: Thu, 05 Sep 2024 03:51:17 GMT  
		Size: 2.7 MB (2693243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111d628735cbf9e5eca437c12fd7cc6f76b05d28f1cfc4838a4fd2f44653e7c4`  
		Last Modified: Thu, 05 Sep 2024 03:51:17 GMT  
		Size: 16.0 KB (16008 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1b7109099c6103a22257ab7f732707ef845fc6f0a67989c4807ceba99b2195d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb45fb8f999ebaaa2b80cf39b0eac4eb8902bcca088d0b01a03977dfdad5dea0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f156bd9ca57b705ad5e96e289144082c7f8c82a762c36e76687ecd3e4df8155`  
		Last Modified: Thu, 05 Sep 2024 07:45:33 GMT  
		Size: 7.7 MB (7651334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6064cb848bdfe067f703b569368855a4e309be56a0a0b1a82f1789f3cc91517`  
		Last Modified: Thu, 05 Sep 2024 07:45:34 GMT  
		Size: 45.0 MB (44970388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046725bd47beb199c5cd89ef71544f7a4a5ce388ce264527616606211d03f7e3`  
		Last Modified: Thu, 05 Sep 2024 07:45:33 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cdb4f41bda45283d5d9d7830b2c47ed7caf5b5aae280496efde391bc771aa8`  
		Last Modified: Thu, 05 Sep 2024 07:45:33 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696664e65a746ae749cd42c4b6dd94e76a5209ee034226c53abe7f1da0a46184`  
		Last Modified: Thu, 05 Sep 2024 07:45:34 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:4f5efbf4355577b4d4d43b4ce1085973af8b35ed6f9902b61de9fee25a96e684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97f564b9680b8494b3edd8eb407e3f3ebf5f39f90d211eeb064a335c5145098`

```dockerfile
```

-	Layers:
	-	`sha256:b478dc1917e70e25dc2d00e2ee3870f8c530378d7b8fb7d6920bb1d4945ad770`  
		Last Modified: Thu, 05 Sep 2024 07:45:33 GMT  
		Size: 2.7 MB (2691219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256cdc5987648a411480ab67fa588fd9701950278bed583cd0bb7bdc7e0bbf5b`  
		Last Modified: Thu, 05 Sep 2024 07:45:33 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json
