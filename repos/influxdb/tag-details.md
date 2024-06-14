<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.7-data`](#influxdb1107-data)
-	[`influxdb:1.10.7-data-alpine`](#influxdb1107-data-alpine)
-	[`influxdb:1.10.7-meta`](#influxdb1107-meta)
-	[`influxdb:1.10.7-meta-alpine`](#influxdb1107-meta-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.5-data`](#influxdb1115-data)
-	[`influxdb:1.11.5-data-alpine`](#influxdb1115-data-alpine)
-	[`influxdb:1.11.5-meta`](#influxdb1115-meta)
-	[`influxdb:1.11.5-meta-alpine`](#influxdb1115-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8.10`](#influxdb1810)
-	[`influxdb:1.8.10-alpine`](#influxdb1810-alpine)
-	[`influxdb:1.9-data`](#influxdb19-data)
-	[`influxdb:1.9-data-alpine`](#influxdb19-data-alpine)
-	[`influxdb:1.9-meta`](#influxdb19-meta)
-	[`influxdb:1.9-meta-alpine`](#influxdb19-meta-alpine)
-	[`influxdb:1.9.13-data`](#influxdb1913-data)
-	[`influxdb:1.9.13-data-alpine`](#influxdb1913-data-alpine)
-	[`influxdb:1.9.13-meta`](#influxdb1913-meta)
-	[`influxdb:1.9.13-meta-alpine`](#influxdb1913-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.6`](#influxdb276)
-	[`influxdb:2.7.6-alpine`](#influxdb276-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:444ac10d971d0f1970669b7b0be35763bdb9cf2c545d6782194e026081aff592
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a510f3dda221d42b1cfee921ee2b7870a823f93967e08cfd94020bb3cdecc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b89693707242c1725d79dd63ded1d04e353cbd43f2fe946b2cf898fabcfbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006a70ad0c3fa769de0312c86d1532eecebd99e18de8748f37f5f33a4e496588`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af11a09cd38a1bb3193cf005130739729b872e9371b111728e14d28245705a`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e960f8f51a21473b22bd32c2601047f9e68b7bf8e14e36a034510a72932d719`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419980cca3d72ba3679c38400ba2c86c700de0494acff47df58de42017b9d21`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ff6e3fdb3bf5612ed3dbee1f682a7ef0452ef26184183a6e1967dadb15b14`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9430221938ee756fdbbd050baf6402881edae0504923e069b306bfeedabe069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee4490c9a7f01b305f49087644b6b3008198091b92f55b5ee95332b19b9a39f`

```dockerfile
```

-	Layers:
	-	`sha256:19f939e26d52a40100e19584933a7ea0a2cb12754e9d6392b11266cb71ab7426`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2fc2cb802caecbe7105b6f62ac794b55fb5669b6f373c6aa135e4965c0d1d3`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:82dbe88ce511d1e82766fc9c8dffa36a6e5df809879d4d2662a08999cae97619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f26b553900ce1858479a83a57bc7fe7e8bf3da393f0affeb4e062c7bc02715ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46177238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bd49ace02e032d44906f1bb4699694687ca1cef2c52d80647d1b8c49fccf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2284974491a6901d5a66daad9c850c24f6400ec3536c9d2ebad76cb03b731d6`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f6e6b6f873cf27293143b9e38672eb9ac2be7ea0d7ece04ee4b4a07cad94a`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97f0e3f871221e418f4b5f6ba09172ea9c8ae9873da311479efabb72ba861a`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 41.3 MB (41321931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a785b97c0df21d517e739406a03dd6cfa80de9aaea4409103ce9658faa77187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15639e0017302fbbd2ecb05a45a1daee75c4ac2505f7fafbcb5e6fdbfbf1175e`

```dockerfile
```

-	Layers:
	-	`sha256:84a7ba3c9004f2d362810cf7b6d9ad080827777ed1a3a0d975947e53f5e8c97b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 728.0 KB (727989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102390a0e6ce368130954848656074611b4b7f1f29aa6e116bb519063da56b1`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:c2689cd574fcb06ac2ed20c4a08826bcb121847df21771db056973e886a4bdc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bcedf12bdccaec1b53010b19490d0472b607525c711773a0d6237ded731dd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b4f0d377cf9409c9ba1fe8ed1520e03be799f29b1287610f6ee4941db32739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe325bea5fa295da512eefcd28e2c9cd4735c198213bc5d3af11391e7255efcd`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bc5f5918327e11b766749581572bfeb5c907f5f92dc7b68f90d9979c983b8`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 20.1 MB (20095568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6187743f48aede39fcd31cc3fd10ad2252a657cc1df32cf99770bb07da3462`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e221ae9cb90080504a204fee036be9206886567254032197212c240b50eb14`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b8f653b32b0effe2f18c599dc82b23280b2524ab528ce442b402fb498fba8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a20909246843a6051ac311b5a0c5307fcbb07819a615d11b92966d14ae5574`

```dockerfile
```

-	Layers:
	-	`sha256:fa0812bd9ad86da041248a37a207cd084bc31f3eefc0e5dc105c95defc669cf2`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbb188a42ebd5df73a5d9c23c68e6d01bd789a3e2b648132fbd83d9ee72d9d7`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 12.9 KB (12920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:aef5f72ff02d611180dd14a7b642e0be908711c1b34be5a0e8e03ab2fedac8e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cdcba1a2d84708d6cc0a196257968136cf1fd6678c0ef8f6023afabe030cabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24896212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a3c26c9c86df010e5d4a687a47f91dcc4fd03f748ac3322665d18a2bd6e796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add49343fc55d2f6606751192a99955e557bdf2fbf187b9f496ebf652a930d7d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04b9b056eb6ed78c191900752590b6eeac62fb265ce1355b387b1f8e225cb9`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b92feb1683c48d36eab756da22a43affed657ce67772e0f74715beabcb8a8b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 20.0 MB (20042110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5c4eed12698239c9012f6459d894a1e5f257292b2af354adf791ebc1f2c62d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bda331172dd8504154fef1b6dc9bcbd808c222bad6557ce86131364c1d2968`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07edd3bd52c8c17cf11d19d3e115aef86b61d6ba0e76c2eb74bc83e66c391365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa662d3b91538dd46613645bdb5fe77016070282c2a937f47842499091afdb`

```dockerfile
```

-	Layers:
	-	`sha256:fea6e8c0b253bf8985c6ab911b31efb96d9209ae9488ed19b80f743f7032af31`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 665.1 KB (665136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf739b2a8aad94ca9d8d0d929cf2f20dd09f15f50365af04fd8d18c1ba524a3e`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 14.8 KB (14787 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:444ac10d971d0f1970669b7b0be35763bdb9cf2c545d6782194e026081aff592
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a510f3dda221d42b1cfee921ee2b7870a823f93967e08cfd94020bb3cdecc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112245319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b89693707242c1725d79dd63ded1d04e353cbd43f2fe946b2cf898fabcfbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006a70ad0c3fa769de0312c86d1532eecebd99e18de8748f37f5f33a4e496588`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af11a09cd38a1bb3193cf005130739729b872e9371b111728e14d28245705a`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e960f8f51a21473b22bd32c2601047f9e68b7bf8e14e36a034510a72932d719`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419980cca3d72ba3679c38400ba2c86c700de0494acff47df58de42017b9d21`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ff6e3fdb3bf5612ed3dbee1f682a7ef0452ef26184183a6e1967dadb15b14`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9430221938ee756fdbbd050baf6402881edae0504923e069b306bfeedabe069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee4490c9a7f01b305f49087644b6b3008198091b92f55b5ee95332b19b9a39f`

```dockerfile
```

-	Layers:
	-	`sha256:19f939e26d52a40100e19584933a7ea0a2cb12754e9d6392b11266cb71ab7426`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 4.6 MB (4579309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2fc2cb802caecbe7105b6f62ac794b55fb5669b6f373c6aa135e4965c0d1d3`  
		Last Modified: Thu, 13 Jun 2024 18:28:40 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:82dbe88ce511d1e82766fc9c8dffa36a6e5df809879d4d2662a08999cae97619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f26b553900ce1858479a83a57bc7fe7e8bf3da393f0affeb4e062c7bc02715ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46177238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bd49ace02e032d44906f1bb4699694687ca1cef2c52d80647d1b8c49fccf8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2284974491a6901d5a66daad9c850c24f6400ec3536c9d2ebad76cb03b731d6`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f6e6b6f873cf27293143b9e38672eb9ac2be7ea0d7ece04ee4b4a07cad94a`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97f0e3f871221e418f4b5f6ba09172ea9c8ae9873da311479efabb72ba861a`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 41.3 MB (41321931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7e8e25125db82d5694d85cf2de1a239c73e3411dcfe9bcc14da24ba0162c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18d3754c72aa6a7ba01fe23cbb06d46af758b76082dd636547c65bc35da6731`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7e8a2bb8e8e9a80fc0bd5e42b8407ff8d7c7737503511940ae843682b9e2`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a785b97c0df21d517e739406a03dd6cfa80de9aaea4409103ce9658faa77187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.4 KB (744413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15639e0017302fbbd2ecb05a45a1daee75c4ac2505f7fafbcb5e6fdbfbf1175e`

```dockerfile
```

-	Layers:
	-	`sha256:84a7ba3c9004f2d362810cf7b6d9ad080827777ed1a3a0d975947e53f5e8c97b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 728.0 KB (727989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b102390a0e6ce368130954848656074611b4b7f1f29aa6e116bb519063da56b1`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:c2689cd574fcb06ac2ed20c4a08826bcb121847df21771db056973e886a4bdc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bcedf12bdccaec1b53010b19490d0472b607525c711773a0d6237ded731dd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90961944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b4f0d377cf9409c9ba1fe8ed1520e03be799f29b1287610f6ee4941db32739`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe325bea5fa295da512eefcd28e2c9cd4735c198213bc5d3af11391e7255efcd`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538bc5f5918327e11b766749581572bfeb5c907f5f92dc7b68f90d9979c983b8`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 20.1 MB (20095568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6187743f48aede39fcd31cc3fd10ad2252a657cc1df32cf99770bb07da3462`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e221ae9cb90080504a204fee036be9206886567254032197212c240b50eb14`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b8f653b32b0effe2f18c599dc82b23280b2524ab528ce442b402fb498fba8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a20909246843a6051ac311b5a0c5307fcbb07819a615d11b92966d14ae5574`

```dockerfile
```

-	Layers:
	-	`sha256:fa0812bd9ad86da041248a37a207cd084bc31f3eefc0e5dc105c95defc669cf2`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 4.5 MB (4516194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbb188a42ebd5df73a5d9c23c68e6d01bd789a3e2b648132fbd83d9ee72d9d7`  
		Last Modified: Thu, 13 Jun 2024 18:28:32 GMT  
		Size: 12.9 KB (12920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:aef5f72ff02d611180dd14a7b642e0be908711c1b34be5a0e8e03ab2fedac8e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cdcba1a2d84708d6cc0a196257968136cf1fd6678c0ef8f6023afabe030cabea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24896212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a3c26c9c86df010e5d4a687a47f91dcc4fd03f748ac3322665d18a2bd6e796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add49343fc55d2f6606751192a99955e557bdf2fbf187b9f496ebf652a930d7d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c04b9b056eb6ed78c191900752590b6eeac62fb265ce1355b387b1f8e225cb9`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 1.2 MB (1231162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b92feb1683c48d36eab756da22a43affed657ce67772e0f74715beabcb8a8b`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 20.0 MB (20042110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5c4eed12698239c9012f6459d894a1e5f257292b2af354adf791ebc1f2c62d`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bda331172dd8504154fef1b6dc9bcbd808c222bad6557ce86131364c1d2968`  
		Last Modified: Thu, 06 Jun 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07edd3bd52c8c17cf11d19d3e115aef86b61d6ba0e76c2eb74bc83e66c391365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa662d3b91538dd46613645bdb5fe77016070282c2a937f47842499091afdb`

```dockerfile
```

-	Layers:
	-	`sha256:fea6e8c0b253bf8985c6ab911b31efb96d9209ae9488ed19b80f743f7032af31`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 665.1 KB (665136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf739b2a8aad94ca9d8d0d929cf2f20dd09f15f50365af04fd8d18c1ba524a3e`  
		Last Modified: Thu, 06 Jun 2024 21:56:29 GMT  
		Size: 14.8 KB (14787 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:81b5ad6321a313fe7f82a7c34276cd6fe72ffa18223a5367f9f03c521d165e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f057f85707e88d4526ed6a1d5fa0c06c8292063847ddd73636f31630af3bb907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21912531e87eaa668568594fdfe9ed9974a267b80b7e7dc6084df2dba3e13f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a86055641dc24259b5c02d9931a17cf67483bcb3ca83e648c6394116a7fc2`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925d31b68388a415295462ccc507bc225784e8c72c6948d746b1dc7034e3162`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 41.8 MB (41822688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d1b873d3cdefbcf10f7079ac83024b97f7ba67599ee47bad9accb57188878`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f6f6cf8334a813f05b6d7b51a4a588d9d664a707ee6c61002a224c72b8e3e7`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2eb468c01062e48661761acf6b87176853cac5b90a1f3214d88f57e12bb081`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c28e5f0926c58e9af2de1e30a15540dec5c25b5166a067603d584902e5d3af10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a74de3c17d68b0fcdde108e9fd466a909fccea7e81e5bd1638544ef52d9aa7f`

```dockerfile
```

-	Layers:
	-	`sha256:3d93801a7b08e3015eefc8dc425b8d94e2ffc8c2767860383f86d28321b9d310`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6780ac418457fdf075d25b6d65b7c3c621f12288a6eb596f21fb087062522c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:10347cdc44d1021944da150e1b37621afc1c2322f0b827b65acecc607ae94cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:46fd52516bb145642c781a860535d31aa97ac601573f98688a50137bf5b858e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce115663f7b549ac95016d0fc96155f4e63c64b075a5fc53b2643149b3523b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaa2b2dc60a82d6d473406d8e2aa752e20a11dd0342067ba4971fc217d73ad`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 1.2 MB (1231161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c953b4a7cec1eee954ab26c9ec75b8c8fbc1b5814703f6f438cd15837f43a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 41.8 MB (41774485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a59fef432ae186ac3fabed896a5d8361c4f64d829f8fba5d0d704e0ae8e221`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d6a509182619f250e17c1cfe4ca2b443bc22313b89c192bfb7be60bd322dfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534d77225de5fcc8282a85481fa894360df24fefaa6fc44693bfc81075c2ad33`

```dockerfile
```

-	Layers:
	-	`sha256:d6a08932ee1fda6a84cabe4695b2d7c5392c7759762e991321ece4c324c82642`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 727.7 KB (727677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7944243a54df737969e062b596fa6febf361b28c97790e27a2e5c91c3b3df8e5`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:52c8a1612bfb1817fd0af25701f576bc220c87dcc8ad1ef76e8f9652cb4be0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:837cdb359ac6b90948414fa056bb2786e423feec0d12c4a47225d51da23114b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94022063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e2a99085a5f46a1b1d668425daacf77d2d5c66b48934fae5e1ac104a675f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04efdc0ddd8684eb7ca3ecf605fab0c132264cb9e83f7a8b366ce8e1e3eea96`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c193c84c0c0801833f3284bb7d7cf2c44cd820d96935ed3b66985dede0a74f5`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 20.4 MB (20393059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ba9dd5223c9f0c7bab069f2dbcee955b3f40d5da32d4dbcb1223a849cd8db`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4402042ce8b0d8a1efeaeb68a2993e262b3492c0187d812b6e3124b462970153`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:489e37b6936c75d54526311839f5d51a99f3ff6ad07d00e6fda8f238b8bf61e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2218c9cf76f2ecd0bd6f7ee333e1ddf900133a659e22c754e40d39a1721b1b4c`

```dockerfile
```

-	Layers:
	-	`sha256:677087dd3bd16f310a285d49e02b7494b001828c8aa35ab5f53d991fe67bbd45`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6e771742b70b4f9e26c492e0e4955514046357577f252759ce2700770c00c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:3f9cb9a9d759b42c183833963a1e8b0df60b5a3ae819d4fb02fb299f3b7384cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc17c0a02e313b286e811b166e491ebcffd7794e5155e7e76c6eb9a08d061f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25199485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d73240e1037bf36eacf00e87f55744f4365d7b83c6e42bc15046167389eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23102befc785708548d111e6cc1c9a36faeb324b4c5c54ed3a66a7723f1647`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 1.2 MB (1231178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86bedbe2a4646c1cc1b2ba84e5f0506e7fd014831332da3b29e279f558f0790`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 20.3 MB (20345367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fcc6b4e7b1450a084f83a18acefd947866d1abd97cc960d32ec1b1cba1f996`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dddd5c49bb7f165c9f7fcb94646aeb7f8653b2c46280a855c54f497c0905943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15541ce468bab39e1369cdad03bca71892675fa2b2070987e314c98c0e32e592`

```dockerfile
```

-	Layers:
	-	`sha256:c1ec890aa98566f94e3c934b954aec9b21437d101ccd72e04833a6b8b1757f73`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 666.0 KB (666010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1194a449822fdbfc5c2de358308f1abbb4567f55c3d3e2412cb52ccd8c212a`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 14.8 KB (14788 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data`

```console
$ docker pull influxdb@sha256:81b5ad6321a313fe7f82a7c34276cd6fe72ffa18223a5367f9f03c521d165e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f057f85707e88d4526ed6a1d5fa0c06c8292063847ddd73636f31630af3bb907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115452899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21912531e87eaa668568594fdfe9ed9974a267b80b7e7dc6084df2dba3e13f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a86055641dc24259b5c02d9931a17cf67483bcb3ca83e648c6394116a7fc2`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925d31b68388a415295462ccc507bc225784e8c72c6948d746b1dc7034e3162`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 41.8 MB (41822688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d1b873d3cdefbcf10f7079ac83024b97f7ba67599ee47bad9accb57188878`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f6f6cf8334a813f05b6d7b51a4a588d9d664a707ee6c61002a224c72b8e3e7`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2eb468c01062e48661761acf6b87176853cac5b90a1f3214d88f57e12bb081`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c28e5f0926c58e9af2de1e30a15540dec5c25b5166a067603d584902e5d3af10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a74de3c17d68b0fcdde108e9fd466a909fccea7e81e5bd1638544ef52d9aa7f`

```dockerfile
```

-	Layers:
	-	`sha256:3d93801a7b08e3015eefc8dc425b8d94e2ffc8c2767860383f86d28321b9d310`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 4.5 MB (4454546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6780ac418457fdf075d25b6d65b7c3c621f12288a6eb596f21fb087062522c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 14.6 KB (14574 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-data-alpine`

```console
$ docker pull influxdb@sha256:10347cdc44d1021944da150e1b37621afc1c2322f0b827b65acecc607ae94cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:46fd52516bb145642c781a860535d31aa97ac601573f98688a50137bf5b858e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46629791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce115663f7b549ac95016d0fc96155f4e63c64b075a5fc53b2643149b3523b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaa2b2dc60a82d6d473406d8e2aa752e20a11dd0342067ba4971fc217d73ad`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 1.2 MB (1231161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c953b4a7cec1eee954ab26c9ec75b8c8fbc1b5814703f6f438cd15837f43a6`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 41.8 MB (41774485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a59fef432ae186ac3fabed896a5d8361c4f64d829f8fba5d0d704e0ae8e221`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6140dbede20e6e7fd9c9ede9998f7fe1aa6e12e01a8d30b5c517acb15e25c33`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e73028f77aac2fa3b46bc35582c8d6816fe1fc934e09731fc2e497c2c4a040`  
		Last Modified: Thu, 06 Jun 2024 21:56:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d6a509182619f250e17c1cfe4ca2b443bc22313b89c192bfb7be60bd322dfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534d77225de5fcc8282a85481fa894360df24fefaa6fc44693bfc81075c2ad33`

```dockerfile
```

-	Layers:
	-	`sha256:d6a08932ee1fda6a84cabe4695b2d7c5392c7759762e991321ece4c324c82642`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 727.7 KB (727677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7944243a54df737969e062b596fa6febf361b28c97790e27a2e5c91c3b3df8e5`  
		Last Modified: Thu, 06 Jun 2024 21:56:31 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta`

```console
$ docker pull influxdb@sha256:52c8a1612bfb1817fd0af25701f576bc220c87dcc8ad1ef76e8f9652cb4be0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:837cdb359ac6b90948414fa056bb2786e423feec0d12c4a47225d51da23114b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94022063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e2a99085a5f46a1b1d668425daacf77d2d5c66b48934fae5e1ac104a675f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04efdc0ddd8684eb7ca3ecf605fab0c132264cb9e83f7a8b366ce8e1e3eea96`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c193c84c0c0801833f3284bb7d7cf2c44cd820d96935ed3b66985dede0a74f5`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 20.4 MB (20393059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ba9dd5223c9f0c7bab069f2dbcee955b3f40d5da32d4dbcb1223a849cd8db`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4402042ce8b0d8a1efeaeb68a2993e262b3492c0187d812b6e3124b462970153`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:489e37b6936c75d54526311839f5d51a99f3ff6ad07d00e6fda8f238b8bf61e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2218c9cf76f2ecd0bd6f7ee333e1ddf900133a659e22c754e40d39a1721b1b4c`

```dockerfile
```

-	Layers:
	-	`sha256:677087dd3bd16f310a285d49e02b7494b001828c8aa35ab5f53d991fe67bbd45`  
		Last Modified: Thu, 13 Jun 2024 18:28:45 GMT  
		Size: 4.4 MB (4391986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d6e771742b70b4f9e26c492e0e4955514046357577f252759ce2700770c00c`  
		Last Modified: Thu, 13 Jun 2024 18:28:44 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.5-meta-alpine`

```console
$ docker pull influxdb@sha256:3f9cb9a9d759b42c183833963a1e8b0df60b5a3ae819d4fb02fb299f3b7384cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc17c0a02e313b286e811b166e491ebcffd7794e5155e7e76c6eb9a08d061f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25199485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d73240e1037bf36eacf00e87f55744f4365d7b83c6e42bc15046167389eef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.11.5-c1.11.5
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5465a51397ea3eaced4b36f85aa661b9d42b79c6c14d51cfc51ba043689fdb`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23102befc785708548d111e6cc1c9a36faeb324b4c5c54ed3a66a7723f1647`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 1.2 MB (1231178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86bedbe2a4646c1cc1b2ba84e5f0506e7fd014831332da3b29e279f558f0790`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 20.3 MB (20345367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fcc6b4e7b1450a084f83a18acefd947866d1abd97cc960d32ec1b1cba1f996`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfb34e747912d3593151e5c76d35843030410daeffffa5833aa4477b84b5fd`  
		Last Modified: Thu, 06 Jun 2024 21:56:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.5-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dddd5c49bb7f165c9f7fcb94646aeb7f8653b2c46280a855c54f497c0905943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.8 KB (680798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15541ce468bab39e1369cdad03bca71892675fa2b2070987e314c98c0e32e592`

```dockerfile
```

-	Layers:
	-	`sha256:c1ec890aa98566f94e3c934b954aec9b21437d101ccd72e04833a6b8b1757f73`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 666.0 KB (666010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1194a449822fdbfc5c2de358308f1abbb4567f55c3d3e2412cb52ccd8c212a`  
		Last Modified: Thu, 06 Jun 2024 21:56:27 GMT  
		Size: 14.8 KB (14788 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:344806154e3f76736c5d5880838276758bc9c6455ee9952815b51e3c0c8595f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:ce2dfa3b03c14ea8a917cebed2457493f1e586bff15162ebf3de5bc4463430d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125752851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067f69032c84af27d9fe1f4e917f626da1ff2c9d98cab7ebc688dc16f9e88a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d220f7af07d471eec68cd698fe1363ee69a2f7a926bfd50f1eb96ba1bf4dce`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9705621dee45f1f9e5647a7d6ca47e541d2afa241e303d2058bf8b30283192`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 54.9 MB (54885339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b28c35e15bf441fc6995e5c298361ff2c8410779bd74f912d257b8b7809a78`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6a1c1ce75b899a8c47b6fe54f2156c7634d79ce7b5bdf55dd107f4401a2f4`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22644748f9bcbf70be4a399e048e8bcbaa7c30a44d30a80c4082e4966042ff8f`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0ea11133afa3fdf341c29556b5bfb1f3135fb6e93466b467878c2e8f90ee008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc06c4941c99fbbb48a4d94ad9f18f1dc5eea9f9850689a98ea5c8a1ca93b90`

```dockerfile
```

-	Layers:
	-	`sha256:5be49328e38c50cb64b1303f45e70e83c9d75e46b949144ddbe47feded49b688`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666d0f50bfc45d5e5ccaded91de9a2e3cd2fc2500bad83bbac48b4452fbb604b`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:73ed0545d0d7b4750b82348b80637a6ee5b43fa6b5dc1f7119e9385a35b4a5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b6467f69d4c0618ed63f2839f6e74733f26b8485c01aeb6076bd414c30e270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a19f7612bbb72940cdb51cd2101cb18ebfaf1a8626e2a3439a67deaee2a45`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc91d1881f12116fa9079825376d00db58c069f271f70480296f9d73e5f9214`  
		Last Modified: Thu, 13 Jun 2024 19:47:52 GMT  
		Size: 51.6 MB (51612887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee905aa2a8918b373df9724acef14e55cc2f2fe140a30fe2d73af3d023d320aa`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251896ff9028ac4ce43839a2ade13e6d35d725129ceebf2a9e7afa48bd0cefdb`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d8d8854d045b9b1ac6560c4e7d2d326e6745403a6d8559103669152f47856`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:fabf9d73f8a655423f971923ff727ec760097cdfbd3b02e5d5add121cbce8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5004d84faed8b4e29d7a335a9b3cb755e56f075c1b049065db004cefeeb9d822`

```dockerfile
```

-	Layers:
	-	`sha256:a4abcc921434578a4c84c315ac2aa09c27a014254ab11e90e1205c5685eb30fb`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa91e7e749ecac64d2a06978219e9f3620094238c6a58b8f6d4e40ba487ff67e`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1caf2085dba3d9a8bbfa1ec8bea174a870ba8b909153181d5a414b0473410398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a3066ce71bd8b347cafa915f8e86245399256baeb3fe2b3dfb70f1926ec3fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2fb20f9f51757e797e545393f33b973f5dc2a7c1dd712ecf0e5991d5918e8`  
		Last Modified: Thu, 13 Jun 2024 19:05:43 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5ae0423c2e85505018c5b499f925f04388c20431940db3692ae98fb231f2d`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 51.2 MB (51229889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62508be208408a3c8a880e27494c6b9fee7aef78ebc5a9750a056c26db72a2a`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feea3223345147a3e497a14d9aa4e9a05d2f6910c91fff8ec3b156cc683294`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e36e4aebd642d8c367809784144ecdb816bdd8e7725cf71f749711929cecbc`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:646a94f8a3f0346228055dac352d07982eaa0f17455f40c6c135d3455c418cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073640e935c37c6c6b6022684081580d3578edee045177e0e9c2794c4cd1fa80`

```dockerfile
```

-	Layers:
	-	`sha256:61b783c8655800c4db918c6eda2b014773c25666a071a3a83c5aee46a86df699`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 4.5 MB (4462635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b112ed998e8d9a8938adfff07e3e86921b17771130d2468075188c4ad0e01a4b`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:344806154e3f76736c5d5880838276758bc9c6455ee9952815b51e3c0c8595f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:ce2dfa3b03c14ea8a917cebed2457493f1e586bff15162ebf3de5bc4463430d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125752851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0067f69032c84af27d9fe1f4e917f626da1ff2c9d98cab7ebc688dc16f9e88a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d220f7af07d471eec68cd698fe1363ee69a2f7a926bfd50f1eb96ba1bf4dce`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9705621dee45f1f9e5647a7d6ca47e541d2afa241e303d2058bf8b30283192`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 54.9 MB (54885339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b28c35e15bf441fc6995e5c298361ff2c8410779bd74f912d257b8b7809a78`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6a1c1ce75b899a8c47b6fe54f2156c7634d79ce7b5bdf55dd107f4401a2f4`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22644748f9bcbf70be4a399e048e8bcbaa7c30a44d30a80c4082e4966042ff8f`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0ea11133afa3fdf341c29556b5bfb1f3135fb6e93466b467878c2e8f90ee008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc06c4941c99fbbb48a4d94ad9f18f1dc5eea9f9850689a98ea5c8a1ca93b90`

```dockerfile
```

-	Layers:
	-	`sha256:5be49328e38c50cb64b1303f45e70e83c9d75e46b949144ddbe47feded49b688`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 4.5 MB (4463023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666d0f50bfc45d5e5ccaded91de9a2e3cd2fc2500bad83bbac48b4452fbb604b`  
		Last Modified: Thu, 13 Jun 2024 18:28:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:73ed0545d0d7b4750b82348b80637a6ee5b43fa6b5dc1f7119e9385a35b4a5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116752976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b6467f69d4c0618ed63f2839f6e74733f26b8485c01aeb6076bd414c30e270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a19f7612bbb72940cdb51cd2101cb18ebfaf1a8626e2a3439a67deaee2a45`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc91d1881f12116fa9079825376d00db58c069f271f70480296f9d73e5f9214`  
		Last Modified: Thu, 13 Jun 2024 19:47:52 GMT  
		Size: 51.6 MB (51612887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee905aa2a8918b373df9724acef14e55cc2f2fe140a30fe2d73af3d023d320aa`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251896ff9028ac4ce43839a2ade13e6d35d725129ceebf2a9e7afa48bd0cefdb`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7d8d8854d045b9b1ac6560c4e7d2d326e6745403a6d8559103669152f47856`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:fabf9d73f8a655423f971923ff727ec760097cdfbd3b02e5d5add121cbce8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5004d84faed8b4e29d7a335a9b3cb755e56f075c1b049065db004cefeeb9d822`

```dockerfile
```

-	Layers:
	-	`sha256:a4abcc921434578a4c84c315ac2aa09c27a014254ab11e90e1205c5685eb30fb`  
		Last Modified: Thu, 13 Jun 2024 19:47:51 GMT  
		Size: 4.5 MB (4464657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa91e7e749ecac64d2a06978219e9f3620094238c6a58b8f6d4e40ba487ff67e`  
		Last Modified: Thu, 13 Jun 2024 19:47:50 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1caf2085dba3d9a8bbfa1ec8bea174a870ba8b909153181d5a414b0473410398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a3066ce71bd8b347cafa915f8e86245399256baeb3fe2b3dfb70f1926ec3fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 06 Jun 2024 16:24:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2fb20f9f51757e797e545393f33b973f5dc2a7c1dd712ecf0e5991d5918e8`  
		Last Modified: Thu, 13 Jun 2024 19:05:43 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5ae0423c2e85505018c5b499f925f04388c20431940db3692ae98fb231f2d`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 51.2 MB (51229889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62508be208408a3c8a880e27494c6b9fee7aef78ebc5a9750a056c26db72a2a`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feea3223345147a3e497a14d9aa4e9a05d2f6910c91fff8ec3b156cc683294`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e36e4aebd642d8c367809784144ecdb816bdd8e7725cf71f749711929cecbc`  
		Last Modified: Thu, 13 Jun 2024 19:05:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:646a94f8a3f0346228055dac352d07982eaa0f17455f40c6c135d3455c418cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073640e935c37c6c6b6022684081580d3578edee045177e0e9c2794c4cd1fa80`

```dockerfile
```

-	Layers:
	-	`sha256:61b783c8655800c4db918c6eda2b014773c25666a071a3a83c5aee46a86df699`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 4.5 MB (4462635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b112ed998e8d9a8938adfff07e3e86921b17771130d2468075188c4ad0e01a4b`  
		Last Modified: Thu, 13 Jun 2024 19:05:44 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:ff68a78c2613757cc137ec48f7a862c6edb0f5a6a1e3fc52d604cb3e036ddd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8da7b4c9ea4e1290de176a2bc593b08de1c53e678db9858a49c3d8754e4fdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59507670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65603081c7d10c6afa775ed78364a34f726d21ef37ef8c6c58e28410b3886a4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d66e26ed51acf4d96c08bb777b841268e106a7712b3862519b5d7507d4f189`  
		Last Modified: Wed, 01 May 2024 21:52:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1f494dad6160af22c1dc31566a1be8f66250e86a9a9ffcdfbf66c4721973d`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 1.5 MB (1479571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4cfe8a0866f27bab617e5f96f856f1e54bc3c33772f0166fd144e546954d4`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 54.6 MB (54646698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6dd6e0aa4ab870a6f13c45453e45ed0884669946fea824deba36caf1f1f81`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50167d227c71947421041efc1934d2c71aa0be90637fabd044b4649e9b57e25f`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09888d5454928396ab82fa3ccd4f6acfe5853a7f21ef57cbb36fd2cf15fe4632`  
		Last Modified: Wed, 01 May 2024 21:52:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:004a0352a5399a0749e2871e2f4a07d65d4623992bf220a1734b7bc140c399dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1001318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc61e7b8b3073e626ae1040b147a7bf23356fb904652d854e8d2db80126c42`

```dockerfile
```

-	Layers:
	-	`sha256:a34439932d7458286af23f31a01a9f738f9b8afd789a17d697f9eec6f18e02ff`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 983.8 KB (983839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96000468ba486d74f19b0155419e78110d366cf9dba2ea7bf86c977c1475c321`  
		Last Modified: Wed, 01 May 2024 21:52:31 GMT  
		Size: 17.5 KB (17479 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:86ab0b6fb1399dba796baae8053bb25d6d25a05abe290e9653c0db9c7c78b005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:700982e519ea56c8e1939a5165762a25ccff1ae1eeb8ffcd7a6e3279235cd2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60bc6b4ddab6bc9a44ff13c4be3c4b36ac9c9ff88b207d4becede1010bfb7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcc94a6f1fa678d46b0ab818eb0d724838181ccdcd4dcefc6913f747fc905b`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957594b16e0b0064114b23dc1892010a4dc90c0baa98a705648fd577048b7ff9`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 33.3 MB (33288959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef58e8a1f016a39de2d8492b12dad5a839739ebd4cb0848658937b8c74c256b4`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6564b87df9d45ec2f4296c078d8ef71d21b0b481ae66bc5a19783f5adeb3ff`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf028904564dbe0b651cd88b8b37e130c26de6c11d4fdba9ecb9bf29fcef7c`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:74c0ca665848d5667a5c68800b848cbf6d9d4cfdbc510f3954a7a1883555d930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc0f1357d42478766f9631ff434bae81f20feebf611c7c38d2b2781fa2c2d4a`

```dockerfile
```

-	Layers:
	-	`sha256:2cdf29fa10b8b767dd265a5a21f06a7f0e6889e34d17781ba392b5c5f65ded9c`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 4.6 MB (4570029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedddbe8895a149fd54e0a9c9cf1263426f76bdd6f5e05f8dea68b2f58ce79fb`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:db6468154a5c2fbbe34ffb0d38efd7c9a870a56003588cf12dc1fbc58b90a481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4f37acb24d052ce198eb7ce1083813abb22f01f8202f5bf081faee440c166dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0fda022b38aaa46a320dfa0af6faee7bd9ac263a9a5fc7907da77713ae8be6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12e4de679c91ac55b036333ae3df3c7b12b4f8ea0e201a196ca9e54cb76960`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05220e020dc05e32599ac940029afb2a536d1a29bc762235ed55e7d974815233`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.8 MB (12769376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f6c7c8ff780009697525b169a7e4c675c5eb2cc162aeee8a908c38612871a`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750c2dafce9732d56e9a48237d3d4617e45cba04f79038a6160d5e4091f6d66`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ae3fba0e0e6878bcb4371cbfa38d73b9d1ac3647f8487ae54144c9c96e4ab662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8adfb69fa1f01e89c76919176b0e1fe11f6f33d09b23f0dcfc17f7bffe67a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c3c908bd9f48dd21ccec96bb5e6f68bd23332a49302c0aa74f59d5752293c4`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94daa159ccd76def86bce20750751f925b5eb1d7cf745fde1a6b22ff21f51384`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.9 KB (12887 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:1b988a39553029f0bdd6abc331bf13dc70ca359a7f570573f5ed597c8cfe2f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d28e68f771b23f1a42ccc0c5a41d51f6fc26e18a8a5b4d097df1cfbce92b409c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17575143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c330ed5ebe2d5f5c13a339f8660db7fce3609a6ad5dae0b52844e70befd9c7a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca6dd7051ee7f68a65b6f526c520d7748a90caa86cbdffd6b5c0587146eff3`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7049e1fb7b4e8eaa01278c751bafb8a2741ff71e0fa3b0a313eb5548dac9f8c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.2 MB (1231172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190ac27b31bcd850f607a58866ce468cdd30626775496c6c5a18168cbe3bde43`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.7 MB (12721034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5969988800f5af670dd7a82fc89ef02efa8ba006a5f37752a933398a6f6df6`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354dcac742097e22fa8705281d1416f95fb9565d0ec7875d0145d8abcf653ddb`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:96170d06a9ac04fb15e1943cf2a34158a7c240ca2a92552a080b8fd3a4de88b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3001c8af2bcc056c0ad7c31848d3f4f924b5d2f89ca8989a9a4564a06388b9c5`

```dockerfile
```

-	Layers:
	-	`sha256:d43dfb2e96983635dd31adde7770bc168a3861bb57b7423ee15d9bffa5842716`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 665.1 KB (665068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bc2bd8f03c533ef8761666da59cdd3a3e7fb3fe59582a708bfe30357b7153`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:86ab0b6fb1399dba796baae8053bb25d6d25a05abe290e9653c0db9c7c78b005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:700982e519ea56c8e1939a5165762a25ccff1ae1eeb8ffcd7a6e3279235cd2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60bc6b4ddab6bc9a44ff13c4be3c4b36ac9c9ff88b207d4becede1010bfb7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcc94a6f1fa678d46b0ab818eb0d724838181ccdcd4dcefc6913f747fc905b`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957594b16e0b0064114b23dc1892010a4dc90c0baa98a705648fd577048b7ff9`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 33.3 MB (33288959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef58e8a1f016a39de2d8492b12dad5a839739ebd4cb0848658937b8c74c256b4`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6564b87df9d45ec2f4296c078d8ef71d21b0b481ae66bc5a19783f5adeb3ff`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf028904564dbe0b651cd88b8b37e130c26de6c11d4fdba9ecb9bf29fcef7c`  
		Last Modified: Thu, 13 Jun 2024 18:28:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:74c0ca665848d5667a5c68800b848cbf6d9d4cfdbc510f3954a7a1883555d930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc0f1357d42478766f9631ff434bae81f20feebf611c7c38d2b2781fa2c2d4a`

```dockerfile
```

-	Layers:
	-	`sha256:2cdf29fa10b8b767dd265a5a21f06a7f0e6889e34d17781ba392b5c5f65ded9c`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 4.6 MB (4570029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedddbe8895a149fd54e0a9c9cf1263426f76bdd6f5e05f8dea68b2f58ce79fb`  
		Last Modified: Thu, 13 Jun 2024 18:28:30 GMT  
		Size: 14.5 KB (14541 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:15d7365e6227e9431db5579e8f141482364c3046af6a1d6be52af335fcbafc07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9a0c681e6b278f2e194fbe5452b3459f922d3cb3f2a6d31bfbb90a714ade5e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38109822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbab36ed44522c8d2dec80d16a7ed5a4ffd9e6a44a84054eef7fe7e9637b391`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Tue, 30 Apr 2024 14:27:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a317c2aa42265d50e848acb3635467a3773abf72ae2c7c2b504afe418a10834`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369ee0d89881d654f2528406cf92ff7a8d541ba7266124369ec2bd44d4c0634`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.5 MB (1479528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db38a39344c06c8e1a02dbbf4a37994d0eee0ed0b6f584d8b60956915632f20`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 33.2 MB (33248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae21f968fc95d3825832158c8041d2855e592424710eaf8b5c0b885652f9bc`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483336b199da361cc41931239143ff402ef984b7f73c096c0477f984749bd073`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b27961f871f2793f18147681fef6f317a0770678efdbb10fb5bea9520dddf`  
		Last Modified: Wed, 01 May 2024 21:52:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb120e160467668a6e67f9f7b4c95a286948b5ed2166e8aab1294f5bc0c4b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47692d0f47733e5825af244b172ca4816fb810d11cb8b4db2cbefaf8fd3e3a94`

```dockerfile
```

-	Layers:
	-	`sha256:e67d6e6010f71f6a83aa9d1ce76511d4d3203364f25080bd6d2f637a58678ce0`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 1.1 MB (1098644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c01e8a120720019fadacc05b56d4022f3247730ee5b0c399b93e61f30bf2151`  
		Last Modified: Wed, 01 May 2024 21:52:18 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:db6468154a5c2fbbe34ffb0d38efd7c9a870a56003588cf12dc1fbc58b90a481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:4f37acb24d052ce198eb7ce1083813abb22f01f8202f5bf081faee440c166dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83635750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0fda022b38aaa46a320dfa0af6faee7bd9ac263a9a5fc7907da77713ae8be6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12e4de679c91ac55b036333ae3df3c7b12b4f8ea0e201a196ca9e54cb76960`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05220e020dc05e32599ac940029afb2a536d1a29bc762235ed55e7d974815233`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.8 MB (12769376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f6c7c8ff780009697525b169a7e4c675c5eb2cc162aeee8a908c38612871a`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750c2dafce9732d56e9a48237d3d4617e45cba04f79038a6160d5e4091f6d66`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ae3fba0e0e6878bcb4371cbfa38d73b9d1ac3647f8487ae54144c9c96e4ab662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4529045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8adfb69fa1f01e89c76919176b0e1fe11f6f33d09b23f0dcfc17f7bffe67a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c3c908bd9f48dd21ccec96bb5e6f68bd23332a49302c0aa74f59d5752293c4`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 4.5 MB (4516158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94daa159ccd76def86bce20750751f925b5eb1d7cf745fde1a6b22ff21f51384`  
		Last Modified: Thu, 13 Jun 2024 18:28:28 GMT  
		Size: 12.9 KB (12887 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:1b988a39553029f0bdd6abc331bf13dc70ca359a7f570573f5ed597c8cfe2f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d28e68f771b23f1a42ccc0c5a41d51f6fc26e18a8a5b4d097df1cfbce92b409c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17575143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c330ed5ebe2d5f5c13a339f8660db7fce3609a6ad5dae0b52844e70befd9c7a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Thu, 06 Jun 2024 16:24:41 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca6dd7051ee7f68a65b6f526c520d7748a90caa86cbdffd6b5c0587146eff3`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7049e1fb7b4e8eaa01278c751bafb8a2741ff71e0fa3b0a313eb5548dac9f8c5`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 1.2 MB (1231172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190ac27b31bcd850f607a58866ce468cdd30626775496c6c5a18168cbe3bde43`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 12.7 MB (12721034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5969988800f5af670dd7a82fc89ef02efa8ba006a5f37752a933398a6f6df6`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354dcac742097e22fa8705281d1416f95fb9565d0ec7875d0145d8abcf653ddb`  
		Last Modified: Thu, 06 Jun 2024 21:56:25 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:96170d06a9ac04fb15e1943cf2a34158a7c240ca2a92552a080b8fd3a4de88b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 KB (679881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3001c8af2bcc056c0ad7c31848d3f4f924b5d2f89ca8989a9a4564a06388b9c5`

```dockerfile
```

-	Layers:
	-	`sha256:d43dfb2e96983635dd31adde7770bc168a3861bb57b7423ee15d9bffa5842716`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 665.1 KB (665068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bc2bd8f03c533ef8761666da59cdd3a3e7fb3fe59582a708bfe30357b7153`  
		Last Modified: Thu, 06 Jun 2024 21:56:24 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:8d8eae9bc4eb5db7c4ef41fb1ae3fa03ff8e9bb52d73f36f4c738758a50d54aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:955d89f24208a13237ea6639a0890b561fcf7d7119afcd5fa7cfab0fa9371a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86694141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491c4e6c5b904335a09ab7e7c6b6862bda2361f191a920f6b1984f5677ccf6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cb5878ee6488e66a81f881a4385ffdedbec093fdae7d9c74af42727097279`  
		Last Modified: Fri, 07 Jun 2024 02:47:37 GMT  
		Size: 9.8 MB (9751022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77bb794bfbe4b734bb3d91387c7cd21c37dc6c525e0b3b155dd6bef8e309ac`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c232048582dbb7db8df170578d8006f2911c96c65be609605d5808879f2a3`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12164450e5dadb31e0bd6bdc329c602882e3d5027861418844e3a1fa839c87e1`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 45.7 MB (45722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76194063f90681845e47a0f5a93525560c461abe2129826986655e7059aae04`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2792e159fb9f449dd7e5aab8ce5bcb0bc2026702ac0c83651624e7e88e542`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a068f2af32ff04a5eb45e03401b70a40dda67da2faa1f68dfc6747c7e93bce9`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87cc165bbd0b298be6d8ccb4f67448a5ebad44329a78a0b28b23279f42e6c9d`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:213ed7adb0be45bea4b98aac0018c8a45a76a164151628877db57153df552071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985b6e3aa764084cf7bf2b39913882da25927985fa66ad03cb787d5e7a976d8`

```dockerfile
```

-	Layers:
	-	`sha256:d733450f4dd915bbef9a06e90eafab35c4da25f374b2fd8c2bb9255efc75442b`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 855.8 KB (855783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1536efec89cabe16e168ce3893962213f885c312bcb2961dbf707938cca86d`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:8d8eae9bc4eb5db7c4ef41fb1ae3fa03ff8e9bb52d73f36f4c738758a50d54aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:955d89f24208a13237ea6639a0890b561fcf7d7119afcd5fa7cfab0fa9371a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86694141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491c4e6c5b904335a09ab7e7c6b6862bda2361f191a920f6b1984f5677ccf6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cb5878ee6488e66a81f881a4385ffdedbec093fdae7d9c74af42727097279`  
		Last Modified: Fri, 07 Jun 2024 02:47:37 GMT  
		Size: 9.8 MB (9751022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77bb794bfbe4b734bb3d91387c7cd21c37dc6c525e0b3b155dd6bef8e309ac`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c232048582dbb7db8df170578d8006f2911c96c65be609605d5808879f2a3`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12164450e5dadb31e0bd6bdc329c602882e3d5027861418844e3a1fa839c87e1`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 45.7 MB (45722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76194063f90681845e47a0f5a93525560c461abe2129826986655e7059aae04`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2792e159fb9f449dd7e5aab8ce5bcb0bc2026702ac0c83651624e7e88e542`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a068f2af32ff04a5eb45e03401b70a40dda67da2faa1f68dfc6747c7e93bce9`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87cc165bbd0b298be6d8ccb4f67448a5ebad44329a78a0b28b23279f42e6c9d`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:213ed7adb0be45bea4b98aac0018c8a45a76a164151628877db57153df552071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985b6e3aa764084cf7bf2b39913882da25927985fa66ad03cb787d5e7a976d8`

```dockerfile
```

-	Layers:
	-	`sha256:d733450f4dd915bbef9a06e90eafab35c4da25f374b2fd8c2bb9255efc75442b`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 855.8 KB (855783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1536efec89cabe16e168ce3893962213f885c312bcb2961dbf707938cca86d`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.6-alpine`

```console
$ docker pull influxdb@sha256:8d8eae9bc4eb5db7c4ef41fb1ae3fa03ff8e9bb52d73f36f4c738758a50d54aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:955d89f24208a13237ea6639a0890b561fcf7d7119afcd5fa7cfab0fa9371a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86694141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491c4e6c5b904335a09ab7e7c6b6862bda2361f191a920f6b1984f5677ccf6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cb5878ee6488e66a81f881a4385ffdedbec093fdae7d9c74af42727097279`  
		Last Modified: Fri, 07 Jun 2024 02:47:37 GMT  
		Size: 9.8 MB (9751022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77bb794bfbe4b734bb3d91387c7cd21c37dc6c525e0b3b155dd6bef8e309ac`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c232048582dbb7db8df170578d8006f2911c96c65be609605d5808879f2a3`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12164450e5dadb31e0bd6bdc329c602882e3d5027861418844e3a1fa839c87e1`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 45.7 MB (45722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76194063f90681845e47a0f5a93525560c461abe2129826986655e7059aae04`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2792e159fb9f449dd7e5aab8ce5bcb0bc2026702ac0c83651624e7e88e542`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a068f2af32ff04a5eb45e03401b70a40dda67da2faa1f68dfc6747c7e93bce9`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87cc165bbd0b298be6d8ccb4f67448a5ebad44329a78a0b28b23279f42e6c9d`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.6-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:213ed7adb0be45bea4b98aac0018c8a45a76a164151628877db57153df552071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985b6e3aa764084cf7bf2b39913882da25927985fa66ad03cb787d5e7a976d8`

```dockerfile
```

-	Layers:
	-	`sha256:d733450f4dd915bbef9a06e90eafab35c4da25f374b2fd8c2bb9255efc75442b`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 855.8 KB (855783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1536efec89cabe16e168ce3893962213f885c312bcb2961dbf707938cca86d`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:8d8eae9bc4eb5db7c4ef41fb1ae3fa03ff8e9bb52d73f36f4c738758a50d54aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7ed3fc60737404a0315136d2a4cf99d746851942d023fcfb83604027cf6c2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18789d716a86c5baac818b929ef561a7a9ff4f1fd745fe14fbd60d1e88df17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47248402b3e64f2df827941ec3a7dfd92267f99eb59d46b20dc1b6925af5104`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c259972c40947eae7e21c8a803f38759499f6a6c86ec1ad536fdcce7af8d159`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 9.6 MB (9630583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e8c5aeb1496e85e6be25ad4e4721c7d1c98693edefe936fab6678bf951bdc`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 5.8 MB (5820947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30584664dad1325b32a5d8807f4e6f4c6be4609b6f286940e1d0949081a4877b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe06acd4aae9b282431a51b05b235d4d6a180213a7596dec693bb657919dde`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 47.6 MB (47621801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645489aaee50f2ed10b4b5e8d57ef53b2f425790ad3222c51c8c49df67ede13`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 23.1 MB (23128280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959b6d1b2ee7931c938ba1e1921252fc4398393c59c41222acb814abaadea93`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6701de9f30f251a1c40a4819fb93a1511299282dd73b07839a8ecf6326162b`  
		Last Modified: Thu, 06 Jun 2024 21:56:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad646e75626fa638d2893fc3e64a9b9031f18f69553389030ac422cbc19b7498`  
		Last Modified: Thu, 06 Jun 2024 21:56:38 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:135fef8b4c86fc6348b54aec0de52f8c7e4815f159407c41da8d6dfe2b9dc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd15ceb5c879375b88d3e2e6f6394d36cf3914d5a22a9cd6a513f77024f6f28`

```dockerfile
```

-	Layers:
	-	`sha256:5f9475980c8c1d912174f5a6b99d3b92c34bee43a9a46b928cd37f5160c178ac`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 856.4 KB (856379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb51c962ad6cca24236a7eb3210985b01fbc184d4f224b2690855a705980d4b`  
		Last Modified: Thu, 06 Jun 2024 21:56:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:955d89f24208a13237ea6639a0890b561fcf7d7119afcd5fa7cfab0fa9371a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86694141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491c4e6c5b904335a09ab7e7c6b6862bda2361f191a920f6b1984f5677ccf6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cb5878ee6488e66a81f881a4385ffdedbec093fdae7d9c74af42727097279`  
		Last Modified: Fri, 07 Jun 2024 02:47:37 GMT  
		Size: 9.8 MB (9751022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77bb794bfbe4b734bb3d91387c7cd21c37dc6c525e0b3b155dd6bef8e309ac`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c232048582dbb7db8df170578d8006f2911c96c65be609605d5808879f2a3`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12164450e5dadb31e0bd6bdc329c602882e3d5027861418844e3a1fa839c87e1`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 45.7 MB (45722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76194063f90681845e47a0f5a93525560c461abe2129826986655e7059aae04`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2792e159fb9f449dd7e5aab8ce5bcb0bc2026702ac0c83651624e7e88e542`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a068f2af32ff04a5eb45e03401b70a40dda67da2faa1f68dfc6747c7e93bce9`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87cc165bbd0b298be6d8ccb4f67448a5ebad44329a78a0b28b23279f42e6c9d`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:213ed7adb0be45bea4b98aac0018c8a45a76a164151628877db57153df552071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985b6e3aa764084cf7bf2b39913882da25927985fa66ad03cb787d5e7a976d8`

```dockerfile
```

-	Layers:
	-	`sha256:d733450f4dd915bbef9a06e90eafab35c4da25f374b2fd8c2bb9255efc75442b`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 855.8 KB (855783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1536efec89cabe16e168ce3893962213f885c312bcb2961dbf707938cca86d`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
