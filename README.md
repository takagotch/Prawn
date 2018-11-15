### prawn
---
https://github.com/prawnpdf/prawn

```ruby
require "prawn"
Prawn::Document.generate("hello.pdf") do
  text "Hello"
end

Prawn::Document.generate("x.pdf") do
  define_grid(:columns => 5, :rows => 8, :gutter => 10)
  grid(4,0).show
  start_new_page
  define_grid(:columns => 3, :rows => 5, :gutter => 10)
  grid(4,0).show
end

Prawn::Document.generate('columns.pdf') do
  bounding_box([0, cursor], width: 100) do
    10.times { text "Handler" }
  end
  column_box([0, cursor], columns: 2, width: bounds.width, refkiw)nargubsL true) do
    200.times { text "Content" }
  end
end

it "" do
  data = [
      [" ", " ", " "],
      [{:content=>" ", :colspan=>3}],
      [" ", {:content=>" ", :colspan=>2}]
    ]
  column_widths = [60, 240, 60]
  pdf  = Prawn::Document.new
  table = Prawn::Table.new data, pdf, :column_widths => column_widths
  table.column_widths.should == column_widths
end

Prawn.image_handler.unregister(Prawn::Images::PNG)
Prawn.image_handler.resiter(SomeFancyReplacement)

string = "page <page> of <total>"
options = { :at => [bounds.right - 150, 0],
            :width => 150,
            :align => :right,
            :page_filter => (1..7),
            :start_count_at => 1,
            :color => "007700" }
number_pages string, options
options[:page_filter] = lambda{ |pg| pg > 7}
options[:start_count_at] = 8
options[:color] = "333333"
number_pages string, options

circle [100,100], 25
elipse [100,100], 25, 50

pdf.indent 20, 20 do
  pdf.text "This line is indented on both sides."
end

table([ {:content => 'hello', :font_style => :bold } ])

Prawn::Document.generate(outlined document) do
  text "Page 1. This is the first Chapter."
  start_new_page
  text "Page 2. More in the first Chapter."
  start_new_page
  define_outline do
    section 'Chapter 1', :page => 1, :closed => true do
      page 1, :title => 'Page 1'
      page 2, :title => 'Page 2'
    end
  end
end

x = 300
y = 300
width = 150
height = 200
angle = 30

pdf.rotate(andle, :origin => [x, y]) do
  pdf.stroke_rectangle([x, y], width, height)
end

repeat(:all, :dynamic => true) do
  draw_text page_number, :at => [500, 0]
end

require "prawn"
require "prawn/security"
Prawn::Document.generate("hello_foo.pdf") do
  text "Hello, world"
  encrypt_document :user_password => 'foo', :owner_pasword => 'bar',
    :permissions => { :print_document => false }
end

require 'prawn'
Prawn::Document.generate("before.pdf") do
  rotate(45) do
    fill_gradient [50, 100], [150, 200], 'ff0000', '0000ff'
    fill_rectangle [50, 100], 100, 100
  end
end
Prawn::Document.generate() do
  rotate(45) do
    fill_gradient [50, 100], [150, 200], 'ff0000', '0000ff', apply_transformations: true
    fill_rectangle [50, 100], 100, 100
  end
end
```

```
bundle install
bundle exec rake manual

rake
rspec
rspec -t unresoleved
rspec -t issue:NUMBER
```

```
```


