<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.6`](#nats216)
-	[`nats:2.1.6-alpine`](#nats216-alpine)
-	[`nats:2.1.6-alpine3.11`](#nats216-alpine311)
-	[`nats:2.1.6-linux`](#nats216-linux)
-	[`nats:2.1.6-nanoserver`](#nats216-nanoserver)
-	[`nats:2.1.6-nanoserver-1809`](#nats216-nanoserver-1809)
-	[`nats:2.1.6-scratch`](#nats216-scratch)
-	[`nats:2.1.6-windowsservercore`](#nats216-windowsservercore)
-	[`nats:2.1.6-windowsservercore-1809`](#nats216-windowsservercore-1809)
-	[`nats:2.1.6-windowsservercore-ltsc2016`](#nats216-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.11`](#nats21-alpine311)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.11`](#nats2-alpine311)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.11`](#natsalpine311)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:ae5e909c737e97356f6f7f1e64726e1c71ad7757e6b233dd11eab4add54e313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:ae5e909c737e97356f6f7f1e64726e1c71ad7757e6b233dd11eab4add54e313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6`

```console
$ docker pull nats@sha256:b9c592f51efecdb94479f4e7802cdbec64a7a8f0af75cf2d57a5a59fdc0e00fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.6` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-alpine`

```console
$ docker pull nats@sha256:4fba482fe8d164db9d27dbaaec677f6891d226a63b4b76f84d7d3b3d0b5cbae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-alpine3.11`

```console
$ docker pull nats@sha256:4fba482fe8d164db9d27dbaaec677f6891d226a63b4b76f84d7d3b3d0b5cbae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.6-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-linux`

```console
$ docker pull nats@sha256:03f234ed2a5313594568538d4c3f0959cf9a3733c374553d42ff37a17503ebac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-nanoserver`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.6-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-nanoserver-1809`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.6-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-scratch`

```console
$ docker pull nats@sha256:03f234ed2a5313594568538d4c3f0959cf9a3733c374553d42ff37a17503ebac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-windowsservercore`

```console
$ docker pull nats@sha256:0a0363aee1ab915ca6823f0cb8f5064cb561b8bd779b34b2167960a6d8d935d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `nats:2.1.6-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.6-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:186133a96780f6a775e4055406f8770a684424433af78e6189512064438e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.6-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:d35b6c4a3418f8ef1ba66c3bcc1a8b938fa440fd3718b2a63b4f66d4d9e2ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `nats:2.1.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.11`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:0a0363aee1ab915ca6823f0cb8f5064cb561b8bd779b34b2167960a6d8d935d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:186133a96780f6a775e4055406f8770a684424433af78e6189512064438e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:d35b6c4a3418f8ef1ba66c3bcc1a8b938fa440fd3718b2a63b4f66d4d9e2ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:0a0363aee1ab915ca6823f0cb8f5064cb561b8bd779b34b2167960a6d8d935d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:186133a96780f6a775e4055406f8770a684424433af78e6189512064438e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:d35b6c4a3418f8ef1ba66c3bcc1a8b938fa440fd3718b2a63b4f66d4d9e2ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.11`

```console
$ docker pull nats@sha256:edfece479f2c8a76eb0eeeaefdde9296f60e5c3175be1630cf54db9a0d8c6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:5340fd4d99375348b2fd6c66e32a07db10195eea00fdf0d1d00c707582650753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4aaa44326a248cd922a09c7731de97c9240fbd0bcb4696e3a400062fe8b084`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:52:46 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:52:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:52:50 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:52:50 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:52:51 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c56fd9023e8499d0d0f63e64800dd46d3361df5a45a1012f4c1fdb4c766933`  
		Last Modified: Mon, 23 Mar 2020 22:53:45 GMT  
		Size: 4.4 MB (4353826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dbb5be7639cc49fa2119e60b7ea78e140e3c6f1f0f6465b433a7a571f65f4d`  
		Last Modified: Mon, 23 Mar 2020 22:53:43 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:bce00d9d88bc4c6fba21488335026e3102f66ee55daa353311345e5c807b2458
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23480fa7be718a41b7727b4ddc07dde9ddd114da9d7d54e8072b2c408844458`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 31 Mar 2020 20:49:36 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 20:49:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 31 Mar 2020 20:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 31 Mar 2020 20:49:52 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:49:53 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1de55532fc814c4a862e789c611472b72868c4fd20d806e8062eaafe58dd641`  
		Last Modified: Tue, 31 Mar 2020 20:54:29 GMT  
		Size: 4.1 MB (4083724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6c7842c241e086a908b5ff2159b1add2ffd4d10e4ba2b7519709c326d53b3c`  
		Last Modified: Tue, 31 Mar 2020 20:54:28 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d8ffb2c728344088c400e9181eb09f1108fb070524dd338e9a2f2c4fd66e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6482247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70be558ab16121fa945f94a2c26d32fdb2ee24af48ae51fbe323708f83fcc5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:34:22 GMT
ENV NATS_SERVER=2.1.4
# Mon, 23 Mar 2020 22:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 23 Mar 2020 22:35:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 23 Mar 2020 22:35:09 GMT
EXPOSE 4222 6222 8222
# Mon, 23 Mar 2020 22:35:14 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae301dd199a70e455fac8fcfdeda98c28bdedaec0048d29f2a979a533325127e`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 4.1 MB (4061195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473cace7e5b47264fc7b18cd3086405487df7d1cac502a888ac25c20a6ce28dd`  
		Last Modified: Mon, 23 Mar 2020 22:35:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:ae5e909c737e97356f6f7f1e64726e1c71ad7757e6b233dd11eab4add54e313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:aea7cc2831f9abd383f4174e38b17849df3606beea6648d63b824eb2a8b88dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:4ec9c8b5fc9c9f5ea875830d8355ac6e9f93d0e3fe5d374d24a5eb6bdf2608fa
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105092070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7678424b503caf1f5241062780f3e6969a8867e91fa257eff465274911c9568`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:16 GMT
RUN cmd /S /C #(nop) COPY file:5493aca6ccb800df74d7e7b98176527689b02c807794603a1f7dde376217279b in C:\nats-server.exe 
# Tue, 31 Mar 2020 21:16:18 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e455632008f14f11f8b72d69a1da128950a141735926961bcf2baf8c2ae12c2`  
		Last Modified: Tue, 31 Mar 2020 21:20:05 GMT  
		Size: 4.0 MB (4036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f44539e2ede61bafd54f622e8042099620ea0dafd8c87cf6043d295f17932f6`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bd5a2e51cc12afa370bd2ec9b2ba2c6ad83cb09ce43555d0ba3b3eb497b49`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 835.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e0425975dec676f07849687918818aa9a711883c2e2b6d39f40c1d922b71b`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec1ea0b29e208f3799b3561fef99ab4b126884eeea9301d6c55f699847d80d`  
		Last Modified: Tue, 31 Mar 2020 21:20:04 GMT  
		Size: 825.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:0a0363aee1ab915ca6823f0cb8f5064cb561b8bd779b34b2167960a6d8d935d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:186133a96780f6a775e4055406f8770a684424433af78e6189512064438e47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:e3a5d10d77bb9a35c8167bc655529206d03c0e7dac2c44f3b9da230c165781b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278709759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc6d6411b3c714e63facea2b4da51b0a7c042c7decc5d5634624f90d3f250`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:14:33 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:14:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:15:02 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:16:01 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:16:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:16:03 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:16:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:16:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18957d3bf61a5f19ebc5847b6ca77f7a7863643e54b7101511766974bad6b69`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b302c84191e1df029de15f2967d9a7b53246786fb26544da226b8c607925ff`  
		Last Modified: Tue, 31 Mar 2020 21:19:47 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93836f3c0cffa6b0a37b955c3dce4dafe0642ab66960be80b1d74d406edf25c`  
		Last Modified: Tue, 31 Mar 2020 21:19:48 GMT  
		Size: 4.7 MB (4681616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbfa8e12b45b0c4d7bff5269d1ff7699720245d9e2037149c0477cd7c1a0e6`  
		Last Modified: Tue, 31 Mar 2020 21:19:46 GMT  
		Size: 8.7 MB (8682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1418e16fcf97cee4031be619e7e26ef941739136dd28cd3f04451f9f132a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7ca764c534845927416d06df263615a01f5f7e2a9aee1385322b761f6fc7`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dd1ff508af5046533914bacdc75ddaa7efdd00cc1327c448272dc08014353`  
		Last Modified: Tue, 31 Mar 2020 21:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f9b92198997df236a1495f0fc7bf389f99880eb61de4877d2e67ca58431a`  
		Last Modified: Tue, 31 Mar 2020 21:19:44 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:d35b6c4a3418f8ef1ba66c3bcc1a8b938fa440fd3718b2a63b4f66d4d9e2ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull nats@sha256:93e77d94d5181b2e8ca9efbacd8c6ef9401b54c6c318b9dd23b7e5751e1653d1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5743587455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28335910c356ede194b2dcd9233b435a9cf6f610dd9c49e62c6bab814e302781`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 13:38:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 31 Mar 2020 21:16:26 GMT
ENV NATS_SERVER=2.1.6
# Tue, 31 Mar 2020 21:16:27 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.6/nats-server-v2.1.6-windows-amd64.zip
# Tue, 31 Mar 2020 21:17:26 GMT
RUN Set-PSDebug -Trace 2
# Tue, 31 Mar 2020 21:19:04 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Tue, 31 Mar 2020 21:19:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Tue, 31 Mar 2020 21:19:07 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 21:19:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 31 Mar 2020 21:19:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddde0325982310255792cba68184203cd656b044bf4f46ab5c1ebf779122527`  
		Last Modified: Wed, 18 Mar 2020 13:42:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d2e783014460190d162f128fa5710a117cd9136ff0582c542e645c5f0b10f`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a23ecd71b35608af4c4e06f1857aab4211c34048dde0a2072401bc8421176`  
		Last Modified: Tue, 31 Mar 2020 21:20:23 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9948d714ad0c8a48c12fe7b9becc3fabe09f61d4d66bd75cf77d91316713000e`  
		Last Modified: Tue, 31 Mar 2020 21:20:24 GMT  
		Size: 5.4 MB (5384998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47e480e660c2de16210e4a70aaf550bd0dd240bf43f1766a7049cfe020cf25`  
		Last Modified: Tue, 31 Mar 2020 21:20:30 GMT  
		Size: 9.4 MB (9431821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d276126def9ffa1ac85e80e3ce86f78dc9f815bf1241f060c953972b16fe8459`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6342f41571faf0fe60bbb2d11b642f0a8499c91ee7b7b48806b4851a5ebd95b8`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662962efab83cc3a58e4d9c59b9e23abc78f4f8634c5ea2d5b87034063037ec9`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4c33960d69a58662fa5a7dac06bd5ceaa709df8079062bf9f684318c0c1b0`  
		Last Modified: Tue, 31 Mar 2020 21:20:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
