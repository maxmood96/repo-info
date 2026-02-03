## `debian:forky-backports`

```console
$ docker pull debian@sha256:7d17d9801b65764de9fb146a23d6bfe2ca38fa9db0c9e4404196c3ff08d00f9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:0b79bd9f24ef7a67d098bd9a2784deaabcc362a03fe6750fa370c1efb2cf1238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48655961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9397f052e5294c4ac4142fa5f5d0d6ddba0cc3b8d206ac34e7d49e78f3772427`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5a63b4b43c1afff0d7421d031d0e005739a96950e6683e91164adbd846938`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38361b0ba82c88b67ce88f327d0d4a8cb14936d0393c5821bf1b3b7b96d259c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe8a0cdd744e90841c5ee277d37ca61ededce1132c72154f3e6e81ffb125d84`

```dockerfile
```

-	Layers:
	-	`sha256:12e7a48b2fccdf8eddc2eaeb26382593426920acd048add83925f37da22e9eb2`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 3.2 MB (3150957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf2134bdb56937668417ebdaac24e9be81919ef0ecc2d14b4660449ba893f1b`  
		Last Modified: Tue, 03 Feb 2026 02:16:11 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fee82cd3ff2a271dbda12d3eb8e1b0f894bebdd0a8774ef3ce98c2f75d4793a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45128721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5492346972c2e91fe2da1d439a561f1e643ae86b903f3d3ce4bb4c3c6191d7db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:17:39 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a41adf61a59d65bb732f71b8fa9e215ce26d7adaa7742f1d0d7dd0c7dec51f11`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45128498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db9b4d193840e9fb0ba500a7b05ea5cade2401dc4309375399ce070647a1e5`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b76648d6f6cb8a4cd8d73118557e5d1fbd90e769241b3cbdb773dcad87ffc6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2253ce13b4da95293ac2a30468abfb7bfd6c33953759adeded52fbc89eedf532`

```dockerfile
```

-	Layers:
	-	`sha256:6d4309342ce4ba9349a14d9762754932560be8b0d9a7da9f9421b4368c8d5a1c`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 3.1 MB (3143407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646a0a5925ce00149c9887ea5c41659705ad83610b53d5a5cab2e0c77518cebf`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3125a1fd3f84ee7cdc5e3418992b6099a24cc7de6e3212c8bcb94569c3a4f5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac73f2fae5d7a702ff15772a0fb200aca92298dc996d96c6b505a1c24b434a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c7bba98969f4ee34dfdf708914620c171291f9d921677b5840e7720194cb4`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9d424337cef918d488099519ff237a5d703be428fdd5955ef97b77d953df280b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6481cae960b51f0c3ee4dd627390058f41dfa85d353ebbd54203e792497035a8`

```dockerfile
```

-	Layers:
	-	`sha256:dc83c98f0f525d08cf36b55423a2a69c0dd8dd87b98ada81e3c0cb46f2792029`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.1 MB (3142880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142681315a4baed655fd3b6a8945576a28a73f22d14d69e905235c360110d5cb`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:a596317fad5d442a6ad4642e53a6b5ad76d3307fc925db0945e6bc0870cd80cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d3b04e3d00a812398031e266acd14556837f8b4ce6668a1ccea1392ec0cb3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c741f2ce2a93d66cb9fa655274b898c2aae57b8774cdfcd943c0c23ba51add`  
		Last Modified: Tue, 13 Jan 2026 01:16:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d038db0ccb25e0416315099fd436cc2401cecc43a658cdf4b17a5e59eac52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e544886e1e95cf4de21bb427876c938cf27e89498c59bda3aa9799fc2c241c`

```dockerfile
```

-	Layers:
	-	`sha256:bf95cfb09e8caf75fdd40fb6881755b9b87562e0b0a2ba7f0d8d037685380635`  
		Last Modified: Tue, 13 Jan 2026 01:16:36 GMT  
		Size: 3.1 MB (3139243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287936192ceb3d37d902fb4931bf7c3a7f963e400420a1caf70c42d9fe16ebc`  
		Last Modified: Tue, 13 Jan 2026 01:16:36 GMT  
		Size: 5.8 KB (5760 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:781c3f7b8be50b770eb85935183eb92da8bb31ec4afb9b55d4f0c0e7a8a55310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53582889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa312940c5314679a39349b200e9c2e94ef8a0302aebc9a000f441696d7cc1ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a0a026d4bb771de47d622d680861a5062bd4e0c02e6c2d817a503a12b7411ab`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 53.6 MB (53582665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38fcfc8e009a023f698b2aaa5bda6c2ceb68bbe28c22cdc1b959ecde4ebec17`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1274ee74c1229040a686d23f86e3fac94808ddb06b80a182f5ae9596d4556b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bb6b9bb768f85ebc40c30fa67b3f09337271e0bb4cdbdcd34ef2b73ede9ef`

```dockerfile
```

-	Layers:
	-	`sha256:633145368ce55ba0b37071e3eb674781bd186016d0d1a1c74b84445452e66f47`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 3.2 MB (3154480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45cf4f76e10dd3ad18ae6ed336ef32bf9089ea00c8824e6da22dd888869f1c3`  
		Last Modified: Tue, 03 Feb 2026 02:14:31 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:f451d4695b411f9102ce34de3118930d66c2dc0b6b585df75c9f3792dbf177c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557810dfa53da63142a437854fe76ad2fc9597a3761e48249c9f83f293c820d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Wed, 14 Jan 2026 04:03:34 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:30 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0f696d74d96ec399c468956e1ee94f1fa01dfc59dd3a9f02df83a04f80a517`  
		Last Modified: Wed, 14 Jan 2026 04:04:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa95fde284364994b8e58f824b53d6c139c212aaaf427800c8c610b463ee438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06840bac843257cae22e73e27707d99e409029cb194d87fa6f3dca8b74ecf218`

```dockerfile
```

-	Layers:
	-	`sha256:225c4abc6dc48755ab71b9d3b7fa664457807c2e131a22a6f9daad91be15f269`  
		Last Modified: Wed, 14 Jan 2026 04:04:29 GMT  
		Size: 3.1 MB (3133537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d81530a876e6438436c53ebfe68ecf92a6e6da9c189eb58576a3afa74b0cdf`  
		Last Modified: Wed, 14 Jan 2026 04:04:28 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:916753e7eac3becf7bd138bb94a571920ad9ef1b22622cda5c99c6e9ee1f8157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48429556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db09a64cabd952b41d70edac9791a252ddd9474c69bc07f0f292903dca68d411`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:15:15 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:616d765aba14d266e800a78cc4d0cdbfd95c5d967a141135b80d41a64ad5ee62`  
		Last Modified: Tue, 03 Feb 2026 01:12:49 GMT  
		Size: 48.4 MB (48429330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5be8a80213d43e0a1d74dd392d7086e53f87094dc9abe2ad57b956313d9d2`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d9dd74c50ef601c0b0b5a040be1201a5ba7094d9c1f1e6e430050b517c9e6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d809fc362ccd8e1a1bb386ca97dc9a2fecf0dbbe9439e8752f216fc44d46db`

```dockerfile
```

-	Layers:
	-	`sha256:625f896e07f2ebf4a1d2e34e46736549c162537c71d8333ff56eff5145e7af8f`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 3.2 MB (3152406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fda7e0edf35888deab71d955111577572a872cd1ea8bd33471f1d5bc3735e7a`  
		Last Modified: Tue, 03 Feb 2026 02:15:26 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
