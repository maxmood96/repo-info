## `fsharp:netcore`

```console
$ docker pull fsharp@sha256:8b67e452be26f7bcb6cbd3ef26013fb593acc67deee221a64fbd671638d60d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:e4b285889ae2685bd24e55a09eb07766ea941e18dce846813fa30d605be00cc1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320293427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fec8bfc152be10f54a6913cb4a8484d7529b39db676c77bf5bbf79f9bfc38b`
-	Default Command: `["dotnet","fsi","--readline","-r","\/usr\/lib\/mono\/4.5\/Mono.Posix.dll"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 09:09:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Sat, 28 Dec 2019 09:09:32 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 28 Dec 2019 09:19:47 GMT
RUN MONO_VERSION=6.4.0.198 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Sat, 28 Dec 2019 09:19:47 GMT
WORKDIR /root
# Sat, 28 Dec 2019 09:19:47 GMT
CMD ["fsharpi"]
# Sat, 28 Dec 2019 09:36:04 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Sat, 28 Dec 2019 09:36:04 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Sat, 28 Dec 2019 09:36:04 GMT
ENV NUGET_XMLDOC_MODE=skip
# Sat, 28 Dec 2019 09:36:15 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 09:36:33 GMT
RUN DOTNET_SDK_VERSION=3.0.100 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=766da31f9a0bcfbf0f12c91ea68354eb509ac2111879d55b656f19299c6ea1c005d31460dac7c2a4ef82b3edfea30232c82ba301fb52c0ff268d3e3a1b73d8f7 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Sat, 28 Dec 2019 09:36:34 GMT
ENV DOTNET_CLI_TELEMETRY_OPTOUT=1     DOTNET_RUNNING_IN_CONTAINER=true     DOTNET_USE_POLLING_FILE_WATCHER=true     NUGET_XMLDOC_MODE=skip
# Sat, 28 Dec 2019 09:36:36 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Sat, 28 Dec 2019 09:36:36 GMT
WORKDIR /root
# Sat, 28 Dec 2019 09:36:36 GMT
CMD ["dotnet" "fsi" "--readline" "-r" "/usr/lib/mono/4.5/Mono.Posix.dll"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b528bfaf665efb774ca3f44d92acacf577dede469e95d807529f4bccf7ef871b`  
		Last Modified: Sat, 28 Dec 2019 09:37:45 GMT  
		Size: 155.3 MB (155302682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c4df7cddbc3c5cebd64f2817314ab0fb221a39a69a96bdf40f8f7d3b0da58`  
		Last Modified: Sat, 28 Dec 2019 09:38:43 GMT  
		Size: 17.9 MB (17936273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d83aa6a3004a75670243c55ea5f63a90cacad4de98a8fb29c55f1cebb7663bc`  
		Last Modified: Sat, 28 Dec 2019 09:39:07 GMT  
		Size: 116.1 MB (116069409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98673e543615e4d84753abf04452aac13f07ca5bd27f0ef727f770f4ea1e5a4`  
		Last Modified: Sat, 28 Dec 2019 09:38:40 GMT  
		Size: 3.9 MB (3892789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
