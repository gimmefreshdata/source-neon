node {
    stage 'configure'
        def archiveUrl = 'https://www.dropbox.com/s/xm7anjtuyn84wh7/NEON.zip?dl=1'

    stage 'import'
        sh "wget --no-cache --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
