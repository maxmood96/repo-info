## `varnish:latest`

```console
$ docker pull varnish@sha256:69773370657fcc3e7226dffc0bb2f836d222961c50558143b814e301cf4283e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:2ee9e9c124d8085bfc963e273362c442066dc3181cf918a5c67119510feba398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122307044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2c697207fe9019f226797228b7b080d250277b6f35c4b4fa0126fdebd5bcac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:37:50 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 24 Jun 2026 01:37:50 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Wed, 24 Jun 2026 01:37:50 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 24 Jun 2026 01:37:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 24 Jun 2026 01:37:50 GMT
ENV VARNISH_SIZE=100M
# Wed, 24 Jun 2026 01:37:50 GMT
ENV VSM_NOPID=1
# Wed, 24 Jun 2026 01:37:50 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 24 Jun 2026 01:37:50 GMT
WORKDIR /etc/varnish
# Wed, 24 Jun 2026 01:37:50 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:37:50 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 24 Jun 2026 01:37:50 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 24 Jun 2026 01:37:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 24 Jun 2026 01:37:50 GMT
USER varnish
# Wed, 24 Jun 2026 01:37:50 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 24 Jun 2026 01:37:50 GMT
CMD []
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7dc024da8f30edf9557f18ef6419ad203626cd5ce4a3a9397d63d4969b0607`  
		Last Modified: Wed, 24 Jun 2026 01:38:05 GMT  
		Size: 92.5 MB (92518738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436049d8d282851d94761450cdd0d222c428be27edb69ea05691fe008abd36c8`  
		Last Modified: Wed, 24 Jun 2026 01:38:02 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87df9f4146506b16306a71f10200377b8592704ac248e7a3d4e347a9a578833`  
		Last Modified: Wed, 24 Jun 2026 01:38:02 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4209cbda6909d0f1f2a8459278d1d49d48f260a1ab77fa0643c69a37947b8877`  
		Last Modified: Wed, 24 Jun 2026 01:38:02 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:2b24e7463a51b5f242d7d15e89310e838548fca1e4ffe27a3aac00a62156d317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ca9d74be16044ba63b146b35771800ecb2a01e72bc8705354a07c846b1bb55`

```dockerfile
```

-	Layers:
	-	`sha256:e38e9103cbc3c4825d20c2ca26edcde508f52149307ee5b7ca545ed6546903fa`  
		Last Modified: Wed, 24 Jun 2026 01:38:02 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:982e311c1345274c8abe11cd460e80ff03564be477fac7ae224a19612eb36b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116321715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8340d3d8552db2b56f948adf84f7c982e1ed1c9e6791df82492ed785d63b78a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:54:03 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 24 Jun 2026 02:54:03 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Wed, 24 Jun 2026 02:54:03 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 24 Jun 2026 02:54:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 24 Jun 2026 02:54:03 GMT
ENV VARNISH_SIZE=100M
# Wed, 24 Jun 2026 02:54:03 GMT
ENV VSM_NOPID=1
# Wed, 24 Jun 2026 02:54:03 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 24 Jun 2026 02:54:03 GMT
WORKDIR /etc/varnish
# Wed, 24 Jun 2026 02:54:03 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:54:03 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 24 Jun 2026 02:54:03 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 24 Jun 2026 02:54:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 24 Jun 2026 02:54:03 GMT
USER varnish
# Wed, 24 Jun 2026 02:54:03 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 24 Jun 2026 02:54:03 GMT
CMD []
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09edf6f73589247d635f23aaecb9e2fbae14707831615ff0a6d9941ab9c263a9`  
		Last Modified: Wed, 24 Jun 2026 02:54:18 GMT  
		Size: 86.2 MB (86170284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa54b7c211843ba3173206234ce3f1c509f6a818ff153fb928d92206245d39f9`  
		Last Modified: Wed, 24 Jun 2026 02:54:15 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda31848a9155bf27b9f8c6b20ab49de61d45eca051382f725abd61e0837f3d7`  
		Last Modified: Wed, 24 Jun 2026 02:54:15 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f6fa5b784d101cc5dd715d170cbb91d8576808af884c57903601e430b7fcc`  
		Last Modified: Wed, 24 Jun 2026 02:54:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:04d3b4b3f0eef3e6e3d86b160f5566f2e68b782f8bd7bf796575481aaaef2428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da2d8a4874028f383cf642a563f14da8d9554c3a8f4e5cd67b4f407bf526036`

```dockerfile
```

-	Layers:
	-	`sha256:9b7d9e3c644ccfdc73bc7a975be136df07dd136fc304da9cf5566bedfdf35fa5`  
		Last Modified: Wed, 24 Jun 2026 02:54:15 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json
